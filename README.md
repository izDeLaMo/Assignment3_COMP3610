# COMP 3610 Assignment 3

## LLM-Powered Analytics with Spark and RAG

### Overview

This project implements an intelligent data analytics system that combines:

* **Apache Spark** for distributed data processing
* **RAG (Retrieval-Augmented Generation)** for document-based question answering
* **LLM-based routing** to integrate structured and unstructured data sources

The system allows users to ask natural language questions, which are automatically routed to:

* Structured taxi data (Spark SQL)
* Transportation policy documents (RAG)
* Or a combination of both (HYBRID queries)

---

### Dataset

#### Structured Data

* NYC Yellow Taxi Trip Records (January 2024)

#### Document Corpus

* NYC Taxi & Limousine Commission reports
* NYC Department of Transportation documents
* Transportation policy PDFs

All documents are stored in the `docs/` directory.

---

### Features

#### Part 1: Spark Analytics

* Data cleaning and feature engineering
* Spark SQL queries for insights
* Performance optimization (caching, partitioning)

#### Part 2: RAG Pipeline

* PDF ingestion and text extraction
* Chunking and embedding using sentence-transformers
* Vector search using ChromaDB
* Context-aware answer generation

#### Part 3: Integrated System

* LLM-based query classification (DATA / DOCUMENT / HYBRID)
* Natural language to SQL translation
* End-to-end intelligent query handling

---

### Setup Instructions

1. Clone the repository:

```bash
git clone <your-repo-link>
cd assignment3
```

2. Install dependencies:

```bash
pip install -r requirements.txt
```

3. Run the notebook:

```bash
jupyter notebook assignment3.ipynb
```

---

### Important Notes

* The dataset is downloaded programmatically in the notebook (not stored in the repo).
* ChromaDB files are excluded for reproducibility.
* Ensure internet connection for downloading PDFs and data.


---

### Reflection Summary

The system effectively integrates distributed data processing with document retrieval, enabling flexible and intelligent querying. It performs well on structured analytics and direct document queries, while hybrid queries demonstrate the power of combining both sources. However, limitations include potential inaccuracies in LLM-generated SQL and dependency on retrieval quality in the RAG pipeline. Future improvements could include better evaluation metrics, enhanced embeddings, and more robust query validation.
