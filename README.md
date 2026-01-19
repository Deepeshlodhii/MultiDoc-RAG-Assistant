# Multi‑Format RAG Chatbot using LangChain & Hugging Face

A Retrieval‑Augmented Generation (RAG) chatbot that can ingest **PDF, HTML, and Markdown** documents, build a semantic search index using **FAISS + Hugging Face embeddings**, and answer user queries using a **local LLM** (Transformers) or an API‑based model.

This project is designed to be:

* Free to run (no API required)
* Cross‑platform
* Colab‑friendly
* Portfolio ready

---

## 🚀 Features

* 📂 Load multiple file types simultaneously: **PDF, HTML, MD**
* ✂️ Smart text chunking using RecursiveCharacterTextSplitter
* 🧠 Semantic embeddings with **sentence-transformers (Hugging Face)**
* ⚡ Fast similarity search using **FAISS**
* 🤖 Local LLM support via Hugging Face Transformers
* 💾 Optional persistence of vector database
* 🧪 Works on Google Colab and local machines

---

## 🏗️ Architecture

```
Documents (PDF/HTML/MD)
        ↓
Document Loaders
        ↓
Text Splitter
        ↓
HuggingFace Embeddings
        ↓
FAISS Vector Store
        ↓
Retriever
        ↓
LLM (Local / API)
        ↓
Answer
```

---

## 📁 Project Structure

```
.
├── docs/                     # Input documents (pdf, html, md)
├── Rag_Langchain_Chatbot.ipynb
├── faiss_index/              # (optional) saved vector database
└── README.md
```

---

## 🛠️ Installation

### Option 1: Google Colab (Recommended)

```python
!pip install langchain langchain-community sentence-transformers faiss-cpu transformers accelerate
```

### Option 2: Local (Python 3.9+)

```bash
pip install langchain langchain-community sentence-transformers faiss-cpu transformers accelerate pypdf unstructured
```

---

## ▶️ Usage

1. Place your documents inside the `docs/` folder

   * Supported: `.pdf`, `.html`, `.md`

2. Open the notebook:

```bash
Rag_Langchain_Chatbot.ipynb
```

3. Run all cells top to bottom

4. Ask questions using the provided `ask()` function

Example:

```python
ask("Summarize the main topics in the documents")
```

---

## 📦 Supported File Types

| Type     | Extension   |
| -------- | ----------- |
| PDF      | .pdf        |
| HTML     | .html, .htm |
| Markdown | .md         |

---

## 🧠 Embedding Model

Default:

```
sentence-transformers/all-MiniLM-L6-v2
```

Fast, lightweight, and accurate for semantic search.

---

## 🤖 LLM Options

### Local (default)

* TinyLlama
* Phi‑2
* Gemma‑2B

### API (optional)

* OpenAI
* Groq
* Together AI

---

## 💡 Use Cases

* Chat with personal notes
* Resume / portfolio chatbot
* Research assistant
* Company document QA system
* Knowledge base assistant

---

## ⚙️ Customization

You can easily:

* Add more file types (TXT, DOCX, CSV)
* Switch embedding models
* Use GPU acceleration
* Add Streamlit UI
* Deploy on Hugging Face Spaces

---

## 🧪 Tech Stack

* Python
* LangChain
* Hugging Face Transformers
* Sentence Transformers
* FAISS
* PyPDF
* Unstructured

---

## 📌 Future Improvements

* Web UI using Streamlit
* API server using FastAPI
* Multi-user support
* Hybrid search (BM25 + embeddings)
* Metadata filtering

---

## 👤 Author

**Deepesh Lodhi**

* IIT Delhi
* Machine Learning & AI Enthusiast
* LangChain & RAG Developer

Happy building 🚀
