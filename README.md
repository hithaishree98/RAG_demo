# LangChain_RAG

## 🧠 Overview
This project implements an **AI-powered conversational assistant** capable of answering questions directly from uploaded documents using **Retrieval-Augmented Generation (RAG)**.  
It combines **LangChain**, **ChromaDB**, and **Groq language models** to build a chatbot that retrieves relevant document chunks and generates contextually accurate, human-like responses.

Unlike typical generative models that rely purely on pretrained knowledge, this system grounds its responses in user-provided documents—ensuring **accuracy**, **traceability**, and **domain adaptability**.  

---

## ⚙️ How It Works — RAG Architecture

**Retrieval-Augmented Generation (RAG)** is a two-step pipeline that enhances large language models with an external knowledge base.

1. **Retrieval Phase**  
   - Uploaded documents are split into text chunks.  
   - Each chunk is converted into an **embedding vector** using OpenAI’s embedding model.  
   - These embeddings are stored in a **ChromaDB vector store** for efficient semantic similarity search.

2. **Generation Phase**  
   - When the user asks a question, the query is also embedded and matched against stored vectors.  
   - The top-K relevant chunks are retrieved.  
   - LangChain constructs a contextual prompt combining the user’s question with retrieved knowledge.  
   - The prompt is sent to the **Groq** model, which generates an informed, reference-grounded answer.

---
