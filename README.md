# RAG for Research AI: Intelligent Document Management and Exploration

**Project Overview :** 
The objective of this assignment is to create an end-to-end system for extracting, managing, and interacting with research publications from the CFA Institute Research Foundation, enabling users to explore and analyze information in a seamless and efficient manner. The system begins with an automated data ingestion pipeline, where publication data, including titles, summaries, images, and PDFs, is scraped and stored. The documents are organized in an AWS S3 bucket, while metadata and links are maintained in a Snowflake database for structured access. The ingestion process is automated through Airflow, ensuring that the data retrieval, storage, and database population are efficient, reliable, and scalable.Building on this foundation, a user-facing application is developed using FastAPI and Streamlit, allowing users to interact with the stored documents. Users can explore documents, generate summaries, and conduct Q&A sessions through a multi-modal Retrieval-Augmented Generation (RAG) model that leverages NVIDIA services for on-the-fly summaries and interactive querying. To facilitate document-specific insights, the system includes indexing and search functionalities, allowing users to search within research notes or full document text to extract meaningful information. To ensure accessibility and scalability, the entire application is containerized with Docker and deployed on a public cloud, offering a robust, user-friendly platform that supports efficient document exploration and enhances the research experience.



**Key Technologies :**

AWS S3 , Snowflake , Streamlit, OpenAI, VS code, CodeLabs, Git, Docker, Python , FAISS , llama Index, Apache Airflow, FastAPI, Nvidia LLM

**Desired Outcome or Solution :**

The desired solution is a fully automated and interactive platform that allows for easy ingestion, storage, and retrieval of CFA Institute research publications.
The system should include a pipeline for scraping, storing, and structuring data in AWS S3 and Snowflake, along with an interface built with FastAPI and Streamlit.
Users should be able to browse documents, generate summaries, and conduct Q&A sessions using a multi-modal Retrieval-Augmented Generation (RAG) model.
The platform should provide accurate, document-specific insights, support incremental indexing, and offer efficient search functionality, all accessible through a publicly deployed application.

Components Overview:

Data Ingestion and Database Population
Client-Facing Application using FastAPI and Streamlit
Research Notes Indexing and Search
Deployment and Accessibility

Tools and Technologies:

AWS S3: Storage for images and PDFs from CFA publications.
Snowflake: For structured storage of metadata and processed data.
Airflow: Pipeline automation and scheduling.
FastAPI and Streamlit: Frontend for user interactions.
Docker and Docker Compose: For containerization.
Python and Dependencies (TOML managed): Backend scripting and AI integrations.
NVIDIA Embeddings and OpenAI: For summaries and document embeddings.
FAISS and Llama Index: For vector storage and indexing.

Client-Facing Application
Components

FastAPI Endpoints:
Users can explore available documents and query metadata.
Streamlit UI:
Provides options to browse documents with images and dropdown selection.
Generates summaries and allows querying based on the user's input.
Real-Time Summarization:
Utilizes NVIDIA's API for dynamic summarization.
Question-Answering (QA) Interface:
Multi-modal retrieval and question-answering through OpenAI’s LLM.

Code and Modules

api_Final.py: FastAPI backend to handle API requests and interact with Snowflake and S3.
main_app.py: Streamlit frontend interface for the users.

Research Notes Indexing and Search
Functionality

Incremental Indexing and Storage:

Research notes are created based on QA results and indexed using FAISS and Llama Index for optimized retrieval.
Search Capabilities:

Users can search notes and document text for detailed insights.
Query results include both full documents and indexed research notes for enhanced relevance.

Approach

FAISS for Vector Search: Fast and efficient similarity search.
Llama Index: Manages indexes across various research notes.

Deployment and Accessibility

Setup
Containerization: FastAPI and Streamlit applications are containerized using Docker.
Docker Compose: Deploys services to ensure seamless communication between backend and frontend.

Cloud Deployment on AWS EC2:

Hosted on an EC2 instance with public access to the API and Streamlit application.

Docker Configuration
Dockerfile.fastapi and Dockerfile.streamlit: Builds for FastAPI and Streamlit, respectively.
docker-compose.yml: Manages multi-container deployment.

Challenges and Future Enhancements

Handling Large Scale Data: Scaling S3 storage and Snowflake configurations for larger datasets.
Enhanced QA with Contextual Understanding: Further refining the QA model using advanced embeddings.
User Authentication: Adding authentication for secure access to sensitive research data.

**Architecture diagram :**

![image](https://github.com/user-attachments/assets/8a6d5b50-4e06-4db7-84ad-2aaa9ac7643f)





**Contribution :**

WE ATTEST THAT WE HAVEN’T USED ANY OTHER STUDENTS’ WORK IN OUR 
ASSIGNMENT AND ABIDE BY THE POLICIES LISTED IN THE STUDENT HANDBOOK


**Documentation files Team_9** 

**Code labs** - https://codelabs-preview.appspot.com/?file_id=11kd-nfh1II7Lafn1ePe5I9zrkUU2L0NpWWojPZNoMd0

**Google Doc** - https://docs.google.com/document/d/11kd-nfh1II7Lafn1ePe5I9zrkUU2L0NpWWojPZNoMd0/edit?tab=t.0

**Video** - https://drive.google.com/file/d/1h2B5IQ4b8CGPbwIMJDLo2LwEdr9p_9bD/view?usp=drive_link

**Web Link** - http://10.110.35.159:8501 
