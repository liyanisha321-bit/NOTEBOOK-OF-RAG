# RAG-Based Question Answering
The project demonstrates how RAG can make large business documents easier to search, understand, and interact with using natural-language questions.



##  Project Overview

This project implements a Retrieval-Augmented Generation (RAG) based Question Answering system using a financial document as the knowledge source.

The system retrieves relevant information from the document and uses a Large Language Model to generate a context-based answer.

##  Objective

- Build a RAG-based Question Answering system.
- Process a large document into smaller chunks.
- Generate embeddings for the document chunks.
- Store and retrieve relevant information using FAISS.
- Generate answers using the retrieved context.

##  Project Workflow

**Document Loading → Text Splitting → Embedding Model → Embedding Creation → FAISS Vector Store → Retrieval → RetrievalQA Chain → Answer Generation**

### 1. Loading

The financial document is loaded into the system using a document loader.

### 2. Splitting

The loaded document is split into smaller text chunks using a text splitter. This makes the document easier to process and retrieve relevant information.

### 3. Loading the Embedding Model

The `BAAI/bge-base-en-v1.5` embedding model is loaded to convert text into meaningful numerical vector representations.

### 4. Creating Embeddings

Embeddings are created for the individual text chunks. These embeddings represent the semantic meaning of the document content.

### 5. FAISS Vector Store

The generated embeddings are stored in a FAISS vector store. FAISS is used to retrieve the most relevant document chunks based on the user's query.

### 6. Build the Chain

A `RetrievalQA` chain is created by combining the language model with the FAISS retriever.

The retriever is configured to retrieve the top relevant chunks and provide them as context to the language model.

### 7. Query and Answer Generation

The user submits a question. The system retrieves relevant content from the document and passes the retrieved context to the language model to generate the final answer.

##  Sample Query

**Question:**

> How often does the company review inventory, and what is considered in this inventory calculation?

The system retrieves the relevant information from the document and generates an answer using the retrieved context.

##  Technologies Used

- Python
- LangChain
- Hugging Face
- Sentence Transformers
- FAISS
- Llama 2
- RetrievalQA

##  Key Observations

- Document chunking helps in handling large unstructured text.
- Embeddings enable semantic-based information retrieval.
- FAISS helps retrieve relevant document content efficiently.
- RetrievalQA connects the retrieved context with the language model.
- The generated response is based on the information retrieved from the source document.

##  Conclusion

This project demonstrates how Retrieval-Augmented Generation can be used to interact with large financial documents through natural-language questions.

By combining **document processing, text chunking, embeddings, FAISS retrieval, and Llama 2**, the system provides a practical approach for context-based question answering.

## 🧠 Skills Learned

- Retrieval-Augmented Generation (RAG)
- LangChain
- Text Chunking
- Semantic Embeddings
- FAISS Vector Search
- LLM-based Question Answering
- RetrievalQA
- Prompt-based Generation
