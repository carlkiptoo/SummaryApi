<template>
  <div class="document-summarizer">
    <input
      type="file"
      @change="handleFileUpload"
      accept=".pdf"
      :disabled="isLoading"
    />
    <button
      @click="summarizeDocument"
      :disabled="!selectedFile || isLoading"
      class="submit-btn"
    >
      {{ isLoading ? "Summarizing..." : "Summarize" }}
    </button>
    <div v-if="error" class="error">{{ error }}</div>
    <div v-if="summary" class="summary">
      <h3>Summary</h3>
      <p>{{ summary.data.summary }}</p>
    </div>
  </div>
</template>

<script setup>
import {ref} from 'vue'
import axios from 'axios'

const selectedFile = ref(null)
const isLoading = ref(false)
const error = ref(null)
const summary = ref(null)
const apiToken = 'APY0w0DZ5FAewhBoIhW5WsgxbIQY7iLe970UZ7VwQFBpkAE63kwW7UKbQFxfdfigh'

const handleFileUpload = (event) => {
    selectedFile.value = event.target.files[0]
    error.value = null
    summary.value = null
}

const summarizeDocument = async() => {
    if(!selectedFile.value) {
        error.value = "Please select a file to summarize"
        return
    }
    isLoading.value = true
    error.value = null

    try {
        const formData = new FormData()
        formData.append('file', selectedFile.value)

        const response = await axios.post(
            'https://api.apyhub.com//ai/summarize-documents/file',
            formData,
            {
                headers: {
                    'Content-Type': 'multipart/form-data',
                    'apy-token': apiToken
                }
            }
        )

        summary.value = response.data

    } catch (error) {
        error.value = err.response?.data?.message || 'An error occured while summarizing document'
    } finally {
        isLoading.value = false
    }
}
</script>
