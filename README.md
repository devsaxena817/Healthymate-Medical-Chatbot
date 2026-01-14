# 🩺 HealthyMate – Medical RAG Chatbot

HealthyMate is an AI-powered **medical chatbot** built using **Retrieval-Augmented Generation (RAG)**. It provides accurate, grounded, and safe medical information by answering user queries strictly based on trusted **medical PDF documents**.

The system combines **LangChain**, **Pinecone Vector Database**, **HuggingFace embeddings**, and **Google Gemini LLM**, wrapped in a **Flask web application**.

---

## 🚀 Features

* 📄 Answers grounded in **medical PDFs** (no hallucinations)
* 🔍 Semantic search using **vector embeddings**
* 🧠 Uses **Gemini LLM** for fast and reliable responses
* 🛡️ Strong medical safety & hallucination control
* 💬 Clean chat-based web interface
* ⚡ Offline indexing + online inference (efficient)

---

## 🏗️ Project Architecture

```
HealthyMate/
│
├── data/                  # Medical PDF documents
├── research/              # Experiments & trials (Jupyter notebook)
├── src/
│   ├── __init__.py
│   ├── helper.py          # PDF loading, chunking, embeddings
│   └── prompt.py          # System prompt & safety rules
│
├── static/
│   └── style.css          # UI styling
├── templates/
│   └── chat.html          # Chat interface
│
├── app.py                 # Flask app (runtime chatbot)
├── store_index.py         # One-time PDF indexing script
├── requirements.txt       # Dependencies
├── setup.py               # Package setup
└── templates.sh           # Utility script
```

---

## 🔄 Workflow Overview

### 1️⃣ Offline Indexing (Run Once)

Medical PDFs are processed and stored in Pinecone:

* Load PDFs from `data/`
* Clean and minimize metadata
* Split text into chunks
* Generate embeddings using HuggingFace
* Store vectors in Pinecone

```bash
python store_index.py
```

---

### 2️⃣ Online Chat Flow (Runtime)

1. User enters a medical query
2. Query is embedded using the same embedding model
3. Pinecone retrieves the most relevant chunks
4. Retrieved context is injected into a medical-safe prompt
5. Gemini LLM generates a grounded response
6. Answer is displayed in the chat UI

---

## 🧠 Core Technologies Used

| Component  | Technology                       |
| ---------- | -------------------------------- |
| Backend    | Flask                            |
| LLM        | Google Gemini (gemini-2.5-flash) |
| Embeddings | HuggingFace (all-MiniLM-L6-v2)   |
| Vector DB  | Pinecone                         |
| Framework  | LangChain                        |
| Frontend   | HTML, CSS                        |

---

## 🧩 Prompt Safety & Medical Guardrails

HealthyMate strictly follows these rules:

* ✅ Uses **only retrieved medical context**
* ❌ Does **not guess or hallucinate**
* 🩺 Provides **educational information only**
* 📢 Clearly responds with *"I don't know"* if context is missing
* 👨‍⚕️ Advises consulting medical professionals when needed

---

## ⚙️ Setup & Installation

### 1️⃣ Clone the Repository

```bash
git clone <your-repo-url>
cd HealthyMate
```

### 2️⃣ Install Dependencies

```bash
pip install -r requirements.txt
```

### 3️⃣ Set Environment Variables

Create a `.env` file:

```env
PINECONE_API_KEY=your_pinecone_api_key
GEMINI_API_KEY=your_gemini_api_key
```

### 4️⃣ Index Medical Documents

```bash
python store_index.py
```

### 5️⃣ Run the Application

```bash
python app.py
```

Open in browser:

```
http://localhost:8080
```

---

## 📌 Example Query

> *What are the common symptoms of type 2 diabetes?*

✔ Retrieved from medical PDFs
✔ Answered in clear bullet points
✔ No hallucinated content

---

## 🔮 Future Improvements

* 📚 Source citation with page numbers
* 💾 Chat memory support
* 🔄 Streaming responses
* 🧠 Domain-specific biomedical embeddings
* 🧩 LangGraph multi-agent workflow

---

## 📄 Disclaimer

This chatbot is for **educational purposes only** and is **not a substitute for professional medical advice**. Always consult a qualified healthcare provider for medical concerns.

---

## 👤 Author

**Dev Saxena**
AI / ML & Software Development Enthusiast

---

⭐ If you find this project useful, consider giving it a star!
