### rag-chatbot/README.md

# 🔍 RAG-Powered Document Assistant

A Retrieval-Augmented Generation (RAG) chatbot for querying domain-specific documents such as procurement contracts, architectural briefs, or healthcare regulations.

## 💡 Features
- Chunk and embed documents (PDFs, Word, TXT)
- Store and query using FAISS vector database
- Answer questions using OpenAI GPT or Mistral
- Simple API served with FastAPI

## 🚀 Usage

1. **Clone the repo**
```bash
git clone https://github.com/yourusername/rag-chatbot.git
cd rag-chatbot
```

2. **Install dependencies**
```bash
pip install -r requirements.txt
```

3. **Add your `.env` file** (for OpenAI or other APIs)
```env
OPENAI_API_KEY=your_key_here
```

4. **Place your documents in the data folder**
```
data/sample_contracts/*.pdf
```

5. **Run the FastAPI app**
```bash
uvicorn app.main:app --reload
```

## 🛠️ Stack
- LangChain + FAISS
- OpenAI GPT / Mistral (via API)
- Python + FastAPI
- Optional UI: Streamlit

## 📁 Project Structure
```
rag-chatbot/
├── app/
│   ├── main.py              # FastAPI entry
│   ├── rag_pipeline.py      # Core logic for retrieval + generation
│   ├── data_loader.py       # Loads & chunks docs
│   └── config.py            # Environment and constants
├── data/sample_contracts/   # Input documents
├── vectorstore/             # Persisted FAISS index
├── tests/                   # Unit/integration tests
├── notebooks/               # Dev notebooks
├── Dockerfile
├── requirements.txt
├── .env
└── README.md
```

## 📦 To Do
- [ ] Add Streamlit UI
- [ ] Add ChromaDB backend option
- [ ] Add feedback/rating loop for fine-tuning
- [ ] Deploy on Hugging Face or Render

## 📜 License
MIT
