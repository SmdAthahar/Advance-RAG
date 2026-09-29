# Advance RAG

A collection of implementations and notes covering key components used in Retrieval-Augmented Generation (RAG) systems.

## 01 — Document Loaders

Document Loaders are used to load information from different sources into a format that can be processed by a RAG pipeline.

Common sources include:

- PDF
- CSV
- JSON
- Text files
- Web pages

In LangChain, loaders typically convert this data into `Document` objects containing:

- `page_content` — the actual content
- `metadata` — information about the source or context

This provides a consistent format for the next stages of a RAG pipeline.

## 02 — Text Splitters

Text Splitters divide large documents into smaller, meaningful chunks before they are converted into embeddings.

Effective chunking is important because the quality and context of chunks can directly affect retrieval and, ultimately, the quality of the generated answer.

Key concepts include:

- Chunk size
- Chunk overlap
- Separators
- Recursive splitting
- Semantic splitting
- LLM-based splitting

The repository includes implementations of different text-splitting approaches, including Character, Recursive Character, Document, Semantic, and LLM-based splitters.

## 03 — Embeddings

Embeddings convert text into numerical vector representations that capture the semantic meaning of the content.

This allows RAG systems to compare and retrieve information based on semantic similarity rather than just keyword matching.

Topics covered include:

- Document embeddings
- Query embeddings
- OpenAI embeddings
- `text-embedding-3-small`
- `text-embedding-3-large`
- Custom embedding dimensions

## 04 — Vector Stores

Vector stores are used to store embeddings and efficiently retrieve relevant information based on vector similarity.

The repository includes hands-on implementations using **ChromaDB**, including:

- Adding documents
- Similarity search
- Similarity search with scores
- Updating documents
- Deleting documents
- CRUD operations
- Persisting vector stores

A PDF-to-vector-store pipeline is also implemented:

**PDF → Document Loading → Chunking → Embeddings → ChromaDB → Retrieval**

More topics will be added and this README will be updated as the repository continues to evolve.
