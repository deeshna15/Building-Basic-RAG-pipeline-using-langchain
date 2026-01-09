# Building-Basic-RAG-pipeline-using-langchain
This project demonstrates how to build a **basic Retrieval-Augmented Generation (RAG) pipeline** using **LangChain**, embeddings, and a vector database.  
The system retrieves relevant documents from a knowledge base and generates accurate answers using a Large Language Model (LLM).

---

## 🚀 Project Overview

Retrieval-Augmented Generation (RAG) combines:
- **Information Retrieval** (from documents)
- **Text Generation** (using an LLM)

Instead of relying only on the model’s internal knowledge, RAG improves accuracy by grounding responses in **retrieved documents**.

---
## 🧠 Architecture
<img width="750" height="355" alt="image" src="https://github.com/user-attachments/assets/875f1db1-18cd-4361-b519-2a0ee9f8f498" />
<img width="413" height="343" alt="image" src="https://github.com/user-attachments/assets/176aaf07-4a11-4288-ac70-245a90e3f009" />

---

## 🛠️ Tech Stack

- Python 3.9+
- LangChain
- LangChain Core & Community
- Sentence Transformers
- ChromaDB
- Google Gemini / Open-source LLM
- Pandas

---
## 📦 Installation

Install all required dependencies:

```bash
pip install langchain langchain-core langchain-community \
sentence-transformers chromadb pandas
```
---
## 📂 Project Structure
<img width="307" height="277" alt="image" src="https://github.com/user-attachments/assets/5959229c-fc09-4ad6-b3d6-2284a76d2c0d" />

---
📄 Sample Documents

Each document contains:

page_content → actual text

metadata → source information
``` bash
from langchain_core.documents import Document

documents = [
    Document(
        page_content="RAG combines retrieval with generation to improve LLM responses.",
        metadata={"source": "doc1"}
    )
]
```
---
## 🔍 Key Steps in the RAG Pipeline
1️⃣ Load Documents

Documents are loaded from text files or defined manually.

2️⃣ Split Text

Large documents are split into smaller chunks for better retrieval.

3️⃣ Generate Embeddings

Text chunks are converted into vector embeddings.

4️⃣ Store in Vector Database

Embeddings are stored in ChromaDB for similarity search.

5️⃣ Retrieve Relevant Documents

The retriever fetches the most relevant chunks for a query.

6️⃣ Generate Answer

The LLM uses retrieved documents to generate a contextual response.
---
## Running the Project
Open the notebook:
``` bash
jupyter notebook rag_pipeline.ipynb
```
Run all cells in order

Ask questions like:
What is RAG?
Why are embeddings important?
Which vector database is used?
📤 Output Format

Retrieved documents with source metadata

Final generated answer from the LLM

Example:
``` bash
Retrieved 2 documents
Source: doc1
Source: doc3

Answer:
Retrieval-Augmented Generation improves response accuracy by grounding
LLM outputs in relevant documents.
```
---
## Features

Modular LangChain pipeline

Vector-based document retrieval

Source-aware answers

Easy to extend and customize
---
## Learning Outcomes

Understanding RAG architecture

Hands-on experience with LangChain

Vector databases and embeddings

Practical LLM integration
---
## 📌 Use Cases

AI Chatbots

Document Question Answering

Knowledge Base Assistants

Educational AI Systems

