# 🎥 YouTube Assistant

A powerful AI-powered application that allows you to ask questions about YouTube videos and get intelligent answers based on the video's transcript. Built with Streamlit, LangChain, and OpenAI's GPT-4.

![Python](https://img.shields.io/badge/Python-3.9+-blue.svg)
![Streamlit](https://img.shields.io/badge/Streamlit-1.45+-red.svg)
![OpenAI](https://img.shields.io/badge/OpenAI-GPT--4-green.svg)
![LangChain](https://img.shields.io/badge/LangChain-0.3+-orange.svg)

## ✨ Features

- **🎯 Video Analysis**: Extract and analyze transcripts from any YouTube video
- **🤖 AI-Powered Q&A**: Ask questions about video content using GPT-4
- **📝 Intelligent Responses**: Get detailed, context-aware answers based on video transcripts
- **🌐 Web Interface**: Clean, intuitive Streamlit web application
- **🔒 Secure**: API key management with password protection
- **📊 Vector Search**: Advanced similarity search using FAISS for accurate responses
- **🐳 Docker Support**: Easy deployment with containerization

## 🚀 Quick Start

### Prerequisites

- Python 3.9 or higher
- OpenAI API key ([Get one here](https://platform.openai.com/api-keys))
- YouTube video URL with available transcript

### Installation

1. **Clone the repository**

   ```bash
   git clone https://github.com/yourusername/youtube-assistant.git
   cd youtube-assistant
   ```

2. **Install dependencies**

   ```bash
   pip install -r requirements.txt
   ```

3. **Run the application**

   ```bash
   streamlit run main.py
   ```

4. **Open your browser**
   Navigate to `http://localhost:8501`

### Using Docker

1. **Build the Docker image**

   ```bash
   docker build -t youtube-assistant .
   ```

2. **Run the container**

   ```bash
   docker run -p 8501:8501 youtube-assistant
   ```

## 📖 How to Use

1. **Enter YouTube URL**: Paste a YouTube video URL in the sidebar
2. **Add OpenAI API Key**: Enter your OpenAI API key (securely stored)
3. **Ask Questions**: Type your question about the video content
4. **Get Answers**: Receive detailed, AI-generated responses based on the video transcript

### Example Questions

- "What are the main points discussed in this video?"
- "Can you summarize the key takeaways?"
- "What does the speaker say about [specific topic]?"
- "What are the steps mentioned for [process]?"

## 🏗️ Architecture

The application uses a sophisticated architecture combining multiple AI technologies:

```
YouTube Video URL → Transcript Extraction → Text Chunking → Vector Embeddings → Similarity Search → GPT-4 Response
```

### Core Components

- **YouTube Loader**: Extracts video transcripts using `youtube-transcript-api`
- **Text Processing**: Splits transcripts into manageable chunks using `RecursiveCharacterTextSplitter`
- **Vector Database**: FAISS for efficient similarity search and retrieval
- **Language Model**: OpenAI's GPT-4 for generating intelligent responses
- **Web Interface**: Streamlit for a responsive, user-friendly experience

## 🔧 Technical Details

### Dependencies

- **Streamlit**: Web application framework
- **LangChain**: AI/LLM orchestration framework
- **OpenAI**: GPT-4 language model integration
- **FAISS**: Vector similarity search
- **youtube-transcript-api**: YouTube transcript extraction

### Key Features

- **Chunk Size**: 1000 characters with 100 character overlap for optimal processing
- **Similarity Search**: Retrieves top 4 most relevant document chunks
- **Token Management**: Optimized for GPT-4's 4097 token limit
- **Error Handling**: Robust error handling for missing transcripts and API issues

## 🛠️ Development

### Project Structure

```
youtube-assistant/
├── main.py                 # Streamlit web application
├── langchain_helper.py     # Core AI processing logic
├── requirements.txt        # Python dependencies
├── Dockerfile             # Docker configuration
└── README.md              # Project documentation
```

### Local Development

1. **Set up virtual environment**

   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

2. **Install development dependencies**

   ```bash
   pip install -r requirements.txt
   ```

3. **Run in development mode**

   ```bash
   streamlit run main.py --server.port=8501
   ```

## 🔒 Security & Privacy

- OpenAI API keys are stored securely and not logged
- No video data is permanently stored
- All processing happens in memory
- Transcripts are only used for generating responses

## 🚨 Troubleshooting

### Common Issues

1. **"No transcript found"**
   - Ensure the YouTube video has closed captions or auto-generated transcripts
   - Try a different video URL

2. **"Please add your OpenAI API key"**
   - Verify your API key is correct
   - Ensure you have sufficient credits in your OpenAI account

3. **"Failed to load transcript"**
   - Check if the video is publicly accessible
   - Verify the URL format is correct

### Performance Tips

- Use videos with clear, well-generated transcripts for best results
- Keep questions specific and focused for more accurate answers
- Ensure stable internet connection for API calls

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- [OpenAI](https://openai.com/) for providing the GPT-4 API
- [LangChain](https://langchain.com/) for the AI orchestration framework
- [Streamlit](https://streamlit.io/) for the web application framework
- [FAISS](https://github.com/facebookresearch/faiss) for vector similarity search

## 📞 Support

If you encounter any issues or have questions:

1. Check the [Issues](https://github.com/yourusername/youtube-assistant/issues) page
2. Create a new issue with detailed information
3. Include error messages and steps to reproduce

---

**Made with ❤️ using AI and modern web technologies**
