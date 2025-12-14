# 📚 Context-Aware Question Answering from PDF Books using a Simplified RAG System

## 🧠 Project Overview

This project implements a **Simplified Retrieval-Augmented Generation (RAG)** system for **question answering directly from PDF book content**. The pipeline loads a full book in PDF format, cleans and splits the text into chunks, retrieves the most relevant sections using semantic similarity, and generates accurate answers using a local Large Language Model.

The system is designed for educational and experimental purposes and demonstrates how modern NLP components (embeddings, vector databases, and LLMs) can be combined into an end-to-end RAG workflow.

---

## 🚀 Key Features

* Load and process full **PDF books**
* Text cleaning and normalization
* Manual text chunking with overlap
* Sentence-level embeddings using **Sentence Transformers**
* Semantic similarity search using **FAISS**
* Answer generation using a **local LLM (LLaMA 3 via Ollama)**
* Interactive **Telegram Bot** interface for asking questions
* Fully implemented inside a single Jupyter Notebook

---

## 🏗️ System Architecture (RAG Pipeline)

1. **PDF Loader** – Extract text from a book using PyMuPDF
2. **Text Cleaning** – Remove noise, line breaks, and page artifacts
3. **Chunking** – Split text into overlapping chunks
4. **Embedding** – Convert chunks into dense vectors using `sentence-transformers/all-MiniLM-L6-v2`
5. **Vector Store** – Store and index embeddings using FAISS
6. **Retriever** – Retrieve top-k relevant chunks for a query
7. **Generator** – Generate answers using a local LLM
8. **Interface** – Telegram bot for real-time user interaction

---

## 🛠️ Technologies Used

* Python 3.11
* Jupyter Notebook / Google Colab
* LangChain
* Sentence Transformers
* FAISS (CPU)
* PyMuPDF (PDF processing)
* Ollama + LLaMA 3 (Local LLM)
* python-telegram-bot

---

## 📂 Project Structure

```
├── rag_qa_from_books.ipynb
├── README.md
├── LICENSE
└── book_index/        # FAISS index files
```

---

## ▶️ How to Run

1. Clone the repository:

```bash
git clone https://github.com/<your-username>/<your-repo-name>.git
```

2. Open the notebook:

```bash
jupyter notebook rag_qa_from_books.ipynb
```

3. Install the required libraries (see notebook cells)

4. Make sure **Ollama** is installed and running locally:

```bash
ollama pull llama3:8b
ollama serve
```

5. Run all notebook cells sequentially

6. (Optional) Create a Telegram bot and set your `BOT_TOKEN` as an environment variable

---

## ⚠️ Notes

* This project was tested primarily on **Google Colab**.
* Some dependency conflicts (e.g., `httpx`) may occur in local environments.
* Do **NOT** hardcode your Telegram Bot Token in public repositories.

---

## 🎯 Use Cases

* Book-based question answering
* Educational NLP and RAG demonstrations
* Semantic search over large documents
* Conversational AI using local LLMs

---

## 🔮 Future Work

* Use a vector database like Chroma or Weaviate
* Improve chunking using document structure
* Add evaluation metrics (Exact Match, F1-score)
* Deploy as a web or API-based service
* Support multiple PDFs

---

## 👩‍💻 Author

Developed by **Eman Hisham**

---

## 📄 License

This project is licensed under the **MIT License**.
