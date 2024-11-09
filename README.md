# Grok-RAG

This repository contains the code for a FastAPI-based question-answering (QA) application using LangChain, Qdrant, and Groq. The application provides answers to user queries based on a context-based model and leverages Google Generative AI embeddings for optimized query responses.

## Overview
This ChatQA API combines LangChain's prompt templates and retrieval chains with the Qdrant vector database and Groq LLM. It is designed to provide efficient, contextually relevant answers to user questions using embeddings and retrieval-based approaches.


## Key Features

- **Vector Embedding with Google Generative AI**: Converts queries into embeddings for enhanced retrieval efficiency.
- **Qdrant Vector Database**: Stores and retrieves embeddings, enabling precise and quick query handling.
- **Context-based Answering**: Uses LangChain to fetch context and generate accurate responses.
- **RESTful API Interface**: Implemented using FastAPI for easy integration and scalability.

### Prerequisites

- Python 3.9 or above
- Install dependencies from `requirements.txt`:
  ```bash
  pip install -r requirements.txt
  ```

### Getting Started

1. **Clone the Repository**
   ```bash
   git clone https://github.com/MubashirAI12/grok-RAG.git
   cd grok-RAG
   ```

2. **Set Up Environment Variables**  
   - Add a `.env` file with the following variables:
     ```bash
     GROQ_API_KEY=<your-groq-api-key>
     GOOGLE_API_KEY=<your-google-api-key>
     qdrant_key=<your-qdrant-api-key>
     URL=<your-qdrant-instance-url>
     ```

3. **Run the Application**
   ```bash
   uvicorn main:app --host 127.0.0.1 --port 8000
   ```

4. **Submit a Query**  
   Access the `/chat_qa/` endpoint via `http://127.0.0.1:8000/docs` to test the interactive API. Submit a JSON body like:
   ```json
   {
     "query": "Your question here"
   }
   ```



### Example Request & Response

Submit a POST request to `/chat_qa/`:
```json
{
  "query": "What is the capital of France?"
}
```

Example Response:
```json
{
  "answer": "The capital of France is Paris."
}
```

### Dependencies

- **FastAPI**: For creating RESTful APIs.
- **LangChain**: For building LLM-based QA systems.
- **Qdrant**: Vector storage and retrieval.
- **Groq**: Provides LLM for question answering.
- **Google Generative AI**: For generating embeddings.

---

