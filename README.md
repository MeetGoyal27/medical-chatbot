# 🏥 Medical Chatbot using LangChain, Pinecone, Groq & Flask

An AI-powered Medical Chatbot built using Retrieval-Augmented Generation (RAG). The chatbot retrieves relevant information from a medical knowledge base stored in Pinecone and generates accurate responses using Groq's Llama 3.1 model.

---

## 🚀 Features

- Medical question answering using RAG
- PDF document ingestion
- Semantic search using Pinecone
- HuggingFace Sentence Transformer embeddings
- Groq Llama 3.1 as the Large Language Model
- Flask-based web interface
- Modular project structure
- Easily extendable with additional medical documents

---

## 📂 Project Structure

```
medical-chatbot/
│
├── dataa/                     # Medical PDF documents
├── research/
│   └── trials.ipynb           # Experimentation notebook
│
├── src/
│   ├── helper.py              # PDF loading, chunking, embeddings
│   ├── prompt.py              # System prompt
│   └── __init__.py
│
├── app.py                     # Flask application
├── store_index.py             # Creates Pinecone vector index
├── requirements.txt
├── .env
└── README.md
```

---

# ⚙️ Installation

## Step 1 : Clone Repository

```bash
git clone <your-github-repository>
cd medical-chatbot
```

---

## Step 2 : Create Virtual Environment

```bash
conda create -n medibot_new python=3.10 -y
```

Activate environment

```bash
conda activate medibot_new
```

---

## Step 3 : Install Dependencies

```bash
pip install -r requirements.txt
```

---

## Step 4 : Configure Environment Variables

Create a `.env` file in the project root.

```env
PINECONE_API_KEY=YOUR_PINECONE_API_KEY
GROQ_API_KEY=YOUR_GROQ_API_KEY
```

---

## Step 5 : Add Medical Documents

Place your medical PDF(s) inside the `dataa` folder.

Example

```
dataa/
    The-Gale-Encyclopedia-of-Medicine.pdf
```

---

## Step 6 : Create Vector Database

```bash
python store_index.py
```

This will

- Load PDF documents
- Split text into chunks
- Generate embeddings
- Upload embeddings to Pinecone

---

## Step 7 : Run the Chatbot

```bash
python app.py
```

Open your browser

```
http://localhost:8080
```

---

# 🧠 Tech Stack

- Python
- Flask
- LangChain
- Pinecone
- HuggingFace Embeddings
- Groq API
- Llama 3.1
- Sentence Transformers

---

# ⚙️ RAG Pipeline

```
Medical PDF
      │
      ▼
PDF Loader
      │
      ▼
Text Splitter
      │
      ▼
Embeddings
      │
      ▼
Pinecone Vector Database
      │
      ▼
Retriever
      │
      ▼
Relevant Chunks
      │
      ▼
Groq Llama 3.1
      │
      ▼
Final Answer
```

---

# 📌 Future Improvements

- Conversation memory
- Streaming responses
- Multiple PDF support
- Chat history
- User authentication
- Source citation
- Docker deployment

---

# 👨‍💻 Author

Meet Goyal
