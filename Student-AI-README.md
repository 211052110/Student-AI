# Student AI Assistant

An AI-powered assistant that answers student queries using retrieval-augmented generation, with semantic chunking to reduce hallucinated responses.

## Overview

Traditional Q&A bots often generate confident but incorrect answers when the retrieved context doesn't actually contain the answer. This project focuses on the retrieval layer — using semantic chunking instead of naive fixed-length splitting — to ground responses more reliably in source material.

## Key Result

- **40% reduction in hallucinated responses** compared to a baseline fixed-chunking RAG pipeline

## Tech Stack

- **LangChain** — orchestration, chains, and retrieval pipeline
- **Semantic chunking** — context-aware text splitting for more relevant retrieval
- Python

## How It Works

1. Source documents are split into semantically coherent chunks (rather than arbitrary fixed-size splits)
2. Chunks are embedded and stored for retrieval
3. On a student query, the most relevant chunks are retrieved and passed to the LLM as grounded context
4. The assistant generates an answer constrained to the retrieved context

## Project Structure

```
├── Student_AI.ipynb    # Development notebook — experimentation & evaluation
├── student_ai.py        # Core assistant logic
└── requirements/setup   # (add a requirements.txt if not already present)
```

## Running Locally

```bash
git clone https://github.com/211052110/Student-AI.git
cd Student-AI
pip install -r requirements.txt
python student_ai.py
```

## Team

Built as a 2-person collaborative project.

## Future Improvements

- Add automated evaluation metrics for hallucination rate
- Expand chunking strategy comparisons
- Add a simple UI/API layer for interaction

---
*Feedback and contributions welcome via issues or pull requests.*
