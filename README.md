# AI-RAG-Pipeline-using-n8n-Gemini-Pinecone
is project implements a Retrieval-Augmented Generation (RAG) system using n8n workflow orchestration, Google Gemini models, and Pinecone vector database.

The system automatically ingests documents from Google Drive, converts them into vector embeddings, stores them in a vector database, and enables a conversational AI agent to retrieve relevant information when answering user queries.

By combining vector search with LLM reasoning, the chatbot produces accurate and context-aware responses grounded in real documents instead of relying purely on model generation.

Problem Statement

Traditional chatbots generate answers using only the language model’s internal knowledge, which often leads to hallucinated or inaccurate responses when answering questions about external documents.

This project solves that problem by implementing a Retrieval-Augmented Generation architecture, where:

documents are converted into vector embeddings

stored in a vector database

retrieved dynamically when users ask questions

The retrieved context is then used by the language model to generate reliable answers.

System Architecture

The system is built using two coordinated pipelines:

Document Ingestion Pipeline

When a new document is uploaded to Google Drive, the system automatically processes it and stores it in the vector database.

Google Drive Upload → File Download → Text Splitting → Embedding Generation → Pinecone Vector Storage

Query & Retrieval Pipeline

Users can ask questions through a conversational interface.
ech Stack

Workflow Orchestration

n8n

AI Models

Google Gemini (LLM)

Gemini Embeddings API

Vector Database

Pinecone

Data Source

Google Drive

AI Components

AI Agent

Conversational Memory

Retrieval Tool

Text Chunking

Key Features

Automated document ingestion from Google Drive

Text chunking and embedding generation

Vector storage using Pinecone

Retrieval-Augmented Generation architecture

Conversational AI agent with memory

Reduced hallucination using retrieval-first design

Workflow orchestration using n8n

The AI agent retrieves relevant information from the vector database before generating the final response.

User Query → AI Agent → Vector Search → Context Retrieval → Gemini Response
