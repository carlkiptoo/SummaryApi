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
      <p>{{ summary }}</p>
    </div>
  </div>
</template>
