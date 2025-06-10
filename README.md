# SummaryApi 📄

A web application that intelligently parses and summarizes document content, helping professionals quickly extract key insights from lengthy documents.

## 🚀 Features

- **Document Upload**: Support for multiple document formats (PDF, DOCX, TXT)
- **Intelligent Parsing**: Extracts text content from various document types
- **AI-Powered Summarization**: Generates concise summaries of document content
- **Web Interface**: User-friendly Vue.js frontend for easy document management
- **RESTful API**: Backend API endpoints for document processing
- **Real-time Processing**: Live updates on document processing status

## 🛠️ Tech Stack

**Frontend:**
- Vue.js
- HTML5/CSS3
- JavaScript (ES6+)

**Backend:**
- Node.js
- Express.js
- File processing libraries
- Text summarization algorithms

## 📋 Prerequisites

Before running this application, make sure you have the following installed:

- Node.js (v14 or higher)
- npm or yarn package manager

## 🔧 Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/carlkiptoo/SummaryApi.git
   cd SummaryApi
   ```

2. **Install backend dependencies**
   ```bash
   cd backend
   npm install
   ```

3. **Install frontend dependencies**
   ```bash
   cd ../frontend
   npm install
   ```

4. **Environment Setup**
   ```bash
   # Create environment file
   cp .env.example .env
   
   # Configure your environment variables
   # Add API keys, database URLs, etc.
   ```

## 🚀 Usage

### Development Mode

1. **Start the backend server**
   ```bash
   cd backend
   npm run dev
   ```

2. **Start the frontend development server**
   ```bash
   cd frontend
   npm run serve
   ```

3. **Access the application**
   - Frontend: `http://localhost:8080`
   - Backend API: `http://localhost:3000`

### Production Mode

```bash
# Build frontend
cd frontend
npm run build

# Start production server
cd ../backend
npm start
```


## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 👨‍💻 Author

**Carl Kiptoo**
- GitHub: [@carlkiptoo](https://github.com/carlkiptoo)
- LinkedIn: [Your LinkedIn Profile]

## 🙏 Acknowledgments

- Thanks to the open-source community for various libraries and tools
- Inspiration from document processing and AI summarization research

## 📞 Support

If you have any questions or need help with setup, please open an issue in the GitHub repository.

---

⭐ **Star this repository if you find it helpful!**
