# RAG Chatbot with FAISS, Hugging Face LLM, and LangChain

This project implements a **Retrieval-Augmented Generation (RAG) chatbot** that allows you to upload a PDF, extract its content, create embeddings using Hugging Face models, store them in a **FAISS vector database**, and query the document through a **Hugging Face LLM** integrated with **LangChain**.

---

## Features
- Upload a PDF file and extract text.
- Split text into manageable chunks with **LangChain's RecursiveCharacterTextSplitter**.
- Create embeddings using **Hugging Face Embeddings** (`sentence-transformers/all-MiniLM-L6-v2`).
- Store and query embeddings in **FAISS** (vector similarity search).
- Use a **Hugging Face LLM (`distilgpt2`)** via LangChain for natural language responses.
- Simple user interface powered by **Streamlit**.

---

## Tech Stack
- [Streamlit](https://streamlit.io/) - Web app framework
- [LangChain](https://www.langchain.com/) - RAG and chaining framework
- [FAISS](https://github.com/facebookresearch/faiss) - Vector database
- [Sentence Transformers](https://www.sbert.net/) - Embedding model
- [Transformers (Hugging Face)](https://huggingface.co/docs/transformers/index) - LLMs

---

How it Works

Extract Text → PDF is read with PyPDF2.

Chunking → Text is split using RecursiveCharacterTextSplitter.

Embeddings → Chunks are embedded with HuggingFaceEmbeddings (sentence-transformers/all-MiniLM-L6-v2).

Vector Store → Embeddings are stored in FAISS for similarity search.

Retriever + LLM → Query retrieves relevant chunks, and a Hugging Face LLM (distilgpt2) generates the final answer.
