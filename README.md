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

More topics will be added and this README will be updated as the repository continues to evolve.

