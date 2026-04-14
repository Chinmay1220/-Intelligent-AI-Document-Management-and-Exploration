# RAG for Research AI: Intelligent Document Management and Exploration

An end-to-end platform for extracting, managing, and interacting with research publications from the CFA Institute Research Foundation - enabling users to explore, summarize, and query documents through a multi-modal RAG-powered interface.

---

## Overview

The system automates the ingestion of CFA Institute research publications (titles, summaries, images, PDFs) into AWS S3 and Snowflake, orchestrated via Apache Airflow. A FastAPI + Streamlit application sits on top, allowing users to browse documents, generate summaries, and conduct Q&A sessions using NVIDIA LLMs and OpenAI embeddings.

---

## Architecture

![Architecture Diagram](https://github.com/user-attachments/assets/8a6d5b50-4e06-4db7-84ad-2aaa9ac7643f)

---

## Key Features

- **Automated Data Ingestion** — Scrapes and stores publications in AWS S3 and Snowflake via Airflow pipelines
- **Document Exploration** — Browse publications with metadata, images, and PDF access
- **AI Summarization** — Real-time document summaries using NVIDIA's LLM API
- **Q&A Interface** — Multi-modal Retrieval-Augmented Generation (RAG) using OpenAI
- **Semantic Search** — FAISS and Llama Index for fast, accurate document retrieval
- **Fully Containerized** — Docker + Docker Compose deployment on AWS EC2

---

## Tech Stack

| Category | Tools |
|---|---|
| Storage | AWS S3, Snowflake |
| Orchestration | Apache Airflow |
| Backend | FastAPI, Python |
| Frontend | Streamlit |
| AI / Embeddings | OpenAI, NVIDIA LLM, FAISS, Llama Index |
| DevOps | Docker, Docker Compose, AWS EC2 |
| Version Control | Git |

---

## Project Structure

```
├── api_Final.py          # FastAPI backend — handles API requests, Snowflake & S3 interactions
├── main_app.py           # Streamlit frontend — user interface for browsing and querying
├── Dockerfile.fastapi    # Docker build for FastAPI
├── Dockerfile.streamlit  # Docker build for Streamlit
├── docker-compose.yml    # Multi-container deployment
└── airflow/              # Airflow DAGs for pipeline automation
```

---

## How It Works

### 1. Data Ingestion
- Airflow DAGs scrape CFA Institute publications
- PDFs and images are stored in AWS S3
- Metadata and links are structured in Snowflake

### 2. Document Interaction
- Users browse documents via Streamlit UI
- FastAPI endpoints serve metadata and document content from Snowflake and S3

### 3. AI-Powered Q&A
- Documents are embedded using NVIDIA and OpenAI services
- FAISS handles vector similarity search
- Llama Index manages incremental indexing across research notes
- Users query documents in natural language and get accurate, context-aware answers

### 4. Deployment
- FastAPI and Streamlit are containerized via Docker
- Deployed on AWS EC2 with public access

---

## Getting Started

```bash
# Clone the repo
git clone <your-repo-url>
cd <repo-name>

# Set up environment variables
cp .env.example .env
# Add your AWS, Snowflake, OpenAI, and NVIDIA credentials

# Run with Docker Compose
docker-compose up --build
```

---

## Resources

- [CodeLabs](https://codelabs-preview.appspot.com/?file_id=11kd-nfh1II7Lafn1ePe5I9zrkUU2L0NpWWojPZNoMd0)
- [Documentation](https://docs.google.com/document/d/11kd-nfh1II7Lafn1ePe5I9zrkUU2L0NpWWojPZNoMd0/edit?tab=t.0)
- [Demo Video](https://drive.google.com/file/d/1h2B5IQ4b8CGPbwIMJDLo2LwEdr9p_9bD/view?usp=drive_link)
