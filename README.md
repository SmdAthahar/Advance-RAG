# Advance RAG

A hands-on learning repository focused on understanding and implementing the different components of a **Retrieval-Augmented Generation (RAG)** pipeline.

This repository documents my learning and practice as I build my understanding of RAG step by step — from loading raw data to preparing it for embeddings, retrieval, and generation.

---

## 📌 RAG Learning Progress

- [x] Document Loaders
- [x] Text Splitters
- [ ] Vector Embeddings
- [ ] Vector Databases
- [ ] Retrieval
- [ ] Reranking
- [ ] RAG Pipeline
- [ ] Advanced RAG
- [ ] Agents

---

# 01 — Document Loaders

Document loaders are responsible for loading information from different sources into a format that can be processed by the RAG pipeline.

During this stage, I practiced loading data from different sources such as:

- PDF
- CSV
- JSON
- Text files
- Web pages

### LangChain Document

Most LangChain document loaders return LangChain `Document` objects.

A `Document` mainly contains:

```python
Document(
    page_content="...",
    metadata={...}
)

# 02 — Text Splitters

After loading documents, the next step I practiced was **Text Splitting**.

Large documents cannot always be passed directly into an embedding model. They need to be divided into smaller, meaningful pieces called **chunks**.

The basic RAG flow at this stage is:

Document → Text Splitter → Chunks → Embeddings → Vector Database

## Why Text Splitting Matters

Chunking is not simply about splitting text into a fixed number of characters.

The way a document is divided can affect:

- Retrieval quality
- Context preservation
- Embedding quality
- Answer quality

For example, if related information is split across different chunks, the retriever may retrieve only part of the required context.

Therefore, the goal is to create chunks that are small enough for efficient processing while still preserving meaningful context.



