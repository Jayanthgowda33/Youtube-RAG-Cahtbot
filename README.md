# 🎬 YouTube RAG Chatbot

> Chat with any YouTube video — paste a URL, ask questions, and get context-aware answers powered by LLMs and RAG.

![Python](https://img.shields.io/badge/Python-3.10+-blue?style=flat&logo=python)
![LangChain](https://img.shields.io/badge/LangChain-latest-orange?style=flat)
![FAISS](https://img.shields.io/badge/FAISS-Vector_Search-purple?style=flat)
![Groq](https://img.shields.io/badge/Groq-LLM_API-green?style=flat)
![License](https://img.shields.io/badge/License-MIT-yellow?style=flat)

---

## 🔍 What It Does

This chatbot lets you have a conversation with any YouTube video. Just paste a YouTube URL, and the system automatically extracts the video transcript, indexes it using vector search, and lets you ask natural language questions — getting accurate, context-aware answers from the video content.

**Example:**
> Paste a 1-hour lecture video URL → Ask *"What are the key points about neural networks?"* → Get a precise summary from the exact part of the video that covers it — without watching the whole thing.

---

## ✨ Features

- 🔗 **YouTube URL Input** — Simply paste any YouTube video link to get started
- 📝 **Automatic Transcript Extraction** — Pulls the full transcript from any YouTube video
- 🧠 **Semantic Search** — Finds the most relevant parts of the video using FAISS vector search
- 💬 **Conversational Q&A** — Ask follow-up questions with full conversation context
- ⚡ **Fast LLM Responses** — Powered by Groq API for ultra-low latency answers
- 🔄 **RAG Pipeline** — Answers are always grounded in the actual video content, not hallucinated

---

## 🏗️ How It Works

```
User pastes YouTube URL
          │
          ▼
  Extract Video Transcript
  (youtube-transcript-api)
          │
          ▼
  Split into Text Chunks
  (LangChain TextSplitter)
          │
          ▼
  Generate Embeddings
          │
          ▼
  Store in FAISS Vector DB
          │
     User asks question
          │
          ▼
  Semantic Search → Top Relevant Chunks
          │
          ▼
  Groq LLM → Generate Answer
          │
          ▼
  Context-aware response shown to user
```

---

## 🛠️ Tech Stack

| Layer | Technology |
|-------|-----------|
| Language | Python 3.10+ |
| LLM Framework | LangChain |
| Vector Database | FAISS |
| LLM Provider | Groq API |
| Transcript Extraction | youtube-transcript-api |
| UI | Streamlit |
| Embeddings | HuggingFace / OpenAI Embeddings |

---

## 📁 Project Structure

```
Youtube-RAG-Cahtbot/
├── app.py                  # Main Streamlit app
├── rag_pipeline.py         # RAG logic — chunking, embedding, retrieval
├── transcript_loader.py    # YouTube transcript extraction
├── requirements.txt        # Python dependencies
├── .env.example            # Environment variable template
└── README.md
```

---

## 🚀 Getting Started

### Prerequisites

- Python 3.10 or higher
- A free [Groq API key](https://console.groq.com)

### Installation

```bash
# 1. Clone the repository
git clone https://github.com/Jayanthgowda33/Youtube-RAG-Cahtbot.git
cd Youtube-RAG-Cahtbot

# 2. Create a virtual environment
python -m venv venv
source venv/bin/activate      # On Windows: venv\Scripts\activate

# 3. Install dependencies
pip install -r requirements.txt

# 4. Set up environment variables
cp .env.example .env
# Add your Groq API key to .env
```

### Run the App

```bash
streamlit run app.py
```

Then open your browser at `http://localhost:8501`

---

## 🔑 Environment Variables

Create a `.env` file in the root directory:

```env
GROQ_API_KEY=your_groq_api_key_here
```

---

## 💡 Example Use Cases

- 📚 **Students** — Ask questions about lecture videos without watching the full video
- 🎙️ **Podcasts** — Extract key insights from long podcast episodes
- 📰 **News** — Quickly get facts from news video reports
- 💼 **Meetings** — Query recorded meeting videos for specific information
- 🔬 **Research** — Extract information from conference talks and presentations

---

## 📸 Demo

> _Add a screenshot or GIF of your chatbot in action here_
>
> **Tip:** Record a 30-second demo — paste a YouTube URL, ask a question, show the answer. Upload as a GIF using [ScreenToGif](https://www.screentogif.com/) or record on [Loom](https://loom.com) and paste the link here. This is the single best thing you can do to impress recruiters!

---

## 🚧 Future Improvements

- [ ] Support for multiple videos in one session
- [ ] Chat history export (PDF/TXT)
- [ ] Timestamp references in answers (jump to exact video moment)
- [ ] Support for non-English videos via auto-translation
- [ ] Deploy on Hugging Face Spaces or Streamlit Cloud

---

## 🤝 Contributing

Contributions, issues, and feature requests are welcome!

1. Fork the repo
2. Create your branch (`git checkout -b feature/your-feature`)
3. Commit your changes (`git commit -m 'Add some feature'`)
4. Push to the branch (`git push origin feature/your-feature`)
5. Open a Pull Request

---

## 👤 Author

**Jayanth Gowda S K**
- 📧 gowdajayanth837@gmail.com
- 💼 [LinkedIn](https://linkedin.com/in/jayanth-gowda-b62344351)
- 🐙 [GitHub](https://github.com/Jayanthgowda33)

---

## 📄 License

This project is licensed under the MIT License.

---

⭐ **If you found this useful, please give it a star!**
