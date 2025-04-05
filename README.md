# **Advanced Reasoning with RAG: Hands-On**

## Overview
This repository contains a hands-on tutorial that demonstrates how to use NVIDIA's reasoning model, [Nemotron](https://build.nvidia.com/nvidia/llama-3_1-nemotron-nano-8b-v1), in combination with Retrieval-Augmented Generation (RAG) techniques. The notebook walks you through building an intelligent chatbot capable of answering questions based on a custom knowledge base while leveraging advanced reasoning capabilities.

### What You Will Learn:
1. **Reasoning Models**: Understand how to use NVIDIA's Nemotron reasoning model to process complex queries with dynamic control over reasoning modes (on/off).
2. **RAG Integration**: Learn how to combine retrieval techniques with reasoning models for context-aware and accurate responses.
3. **Custom Knowledge Base**: Explore how to load, transform, and query custom documents (e.g., PDFs) using LangChain.
4. **Hands-On Implementation**: Build a reusable Python class (`QueryExecutor`) to interact with the reasoning model and seamlessly integrate RAG.


---

# **How to Register and Obtain NVIDIA API Access**

To use NVIDIA's Nemotron reasoning model and other AI services in this hands-on tutorial, you need to register for an API key. Follow the steps below to obtain access:



## **Step-by-Step Guide**

1. **Register or Log In**:
   - Go to [NVIDIA Build](https://build.nvidia.com).
   - Create an account (preferably using an academic email address) or log in if you already have one.
   - **Note**: If there are too many simultaneous registrations, the system may temporarily block new accounts. Please try again later if this happens.

2. **Verify API Rate Limit**:
   - After logging in, check the top-right corner of the page. You should see a message like:
     ```
     Your API Rate Limit UP TO 40 RPM
     ```
   - This indicates your current API request rate limit.

3. **Generate an API Key**:
   - Click on **"Manage API Keys"** in your account dashboard.
   - Select **"Generate API Key"**.
   - Provide a name for your key and set an expiration date (optional).

4. **Copy Your API Key**:
   - Once generated, copy your API key (e.g., `nvapi-*****`).
   - You will need this key during the hands-on tutorial to authenticate and interact with NVIDIA's AI models.

## **Important Notes**
- Keep your API key secure and do not share it publicly.
- If you encounter issues during registration or key generation, refer to NVIDIA's support documentation or contact their support team.

With your API key ready, proceed to the hands-on tutorial and paste it into the designated cell when prompted.


---

## Notebook Structure

### 1. **Environment Setup**
   - Install all necessary dependencies for LangChain, NVIDIA AI Foundation Models, and vector store integration.
   - Authenticate using your NVIDIA API key.

### 2. **Loading Documents**
   - Use LangChain's `PyPDFLoader` to load a sample PDF document into memory as a knowledge base.

### 3. **Transforming Documents**
   - Split the document into smaller, manageable chunks using `SentenceTransformersTokenTextSplitter` for efficient processing and embedding generation.

### 4. **Embedding and Vector Store**
   - Generate embeddings for the document chunks and store them in a vector store for fast similarity search.

### 5. **Querying the Reasoning Model**
   - Build a `QueryExecutor` class to interact with the Nemotron reasoning model.
   - Dynamically control reasoning mode (`on`/`off`) and add system-level prompts to guide the model's behavior.

### 6. **Integrating RAG**
   - Combine the vector store retrieval results with the Nemotron model to enable Retrieval-Augmented Generation (RAG).
   - Use retrieved documents as context for generating detailed and accurate responses.

---

## Prerequisites
- Python 3.11 or higher
- NVIDIA API key (Sign up for free credits [here](https://catalog.ngc.nvidia.com/))
- Basic understanding of Python and large language models

---
## Key Features

- **Dynamic Reasoning Control**: Toggle between detailed (`on`) or simple (`off`) reasoning modes.
- **Custom Prompts**: Add system-level instructions to guide model behavior.
- **RAG Integration**: Combine retrieval results with advanced reasoning for context-aware responses.
- **Extensibility**: Easily adapt the `QueryExecutor` class for different use cases or models.

---

## References

- [LangChain Documentation](https://python.langchain.com/docs/)
- [NVIDIA Nemotron Model](https://build.nvidia.com/nvidia/llama-3_1-nemotron-nano-8b-v1)
- [Retrieval-Augmented Generation (RAG)](https://python.langchain.com/docs/modules/data_connection/)
