# End-to-End RAG Chatbot with Databricks, LangChain & Unity Catalog

A production RAG system built during my internship at Thriving Springs AI that enables context-aware natural language querying over enterprise data. The system integrates Databricks, Unity Catalog, and LangChain into a fully automated AI assistant.

> Note: Source code is proprietary to Thriving Springs AI and is not included in this repository.

---

## What It Does

Employees can ask natural language questions against internal enterprise datasets. The system retrieves the most relevant context from a vector store, augments it into a prompt, and generates accurate, grounded answers — eliminating the need for manual data lookups.

---

## Architecture

```
Enterprise Data (PDFs, docs)
          |
          v
Ingestion Pipeline
  - PDF parsing
  - BGE-large-en embedding model
  - Semantic chunking
          |
          v
Databricks Vector Store (Unity Catalog)
          |
          v
User Query
  - Semantic search (top-k retrieval)
  - Advanced prompt engineering
  - Semantic filtering
          |
          v
LangChain LLM Chain
          |
          v
Grounded Answer
```

---

## Key Components

**Embedding & Ingestion Pipeline**
- Documents parsed and chunked for high-precision retrieval
- BGE-large-en embeddings for semantic representation
- Vectors stored and managed via Databricks Unity Catalog

**Retrieval Layer**
- Semantic similarity search over the vector store
- Threshold-based filtering to avoid hallucination on out-of-scope queries
- Advanced prompt engineering to keep answers grounded in retrieved context

**LangGraph Multi-Agent Workflow**
- Schema analysis agent understands the data structure
- SQL generation agent writes optimized queries
- Report summarization agent formats final output
- Dynamic tool orchestration between agents

---

## Results

| Metric | Improvement |
|--------|-------------|
| Retrieval accuracy | +35% over baseline |
| Internal data lookup time | Significantly reduced |
| Manual query handling | Eliminated for common queries |

---

## Tech Stack

| Tool | Purpose |
|------|---------|
| Databricks | Compute, vector store, Unity Catalog |
| LangChain | LLM chaining and retrieval |
| LangGraph | Multi-agent workflow orchestration |
| BGE-large-en | High-precision text embeddings |
| Python | Core implementation language |

---

## Context

Built during an AI Engineer internship at **Thriving Springs AI** (Aug 2025 – Sep 2025).

The system was deployed as an internal AI assistant that automated data lookups and improved team productivity. The architecture decisions — particularly the choice of BGE-large over smaller embedding models and the semantic filtering threshold — were driven by measured accuracy improvements during evaluation.

---

## Author

Ishaan Chowdhury · [@Ishaan20072612](https://github.com/Ishaan20072612)  
AI Engineer Intern — Thriving Springs AI
