# Week 10: RAG (Retrieval Augmented Generation) System

Part of Project 3 (GenAI Domain Assistant) for the Applied AI course, Week 10 lab.

## Overview
Builds a Retrieval Augmented Generation pipeline that answers questions from company policy documents instead of relying on the model's general knowledge.

## What it does
- Loads `.txt` documents from `company_docs/` using LangChain's `DirectoryLoader`
- Splits documents into chunks with `RecursiveCharacterTextSplitter`
- Implements simple keyword-based retrieval (`simple_search`)
- Builds a RAG pipeline (`rag_query`) that retrieves relevant chunks and generates an answer using the Gemini API (`gemini-3.6-flash`)
- Compares answers with vs. without RAG to show the value of grounding responses in real documents

## Tech stack
- LangChain (document loading, text splitting)
- Google Gemini API (`google-genai`)
- Jupyter Notebook

## Files
- `week10_rag_system.ipynb` — main notebook with all lab tasks
- `company_docs/` — sample company policy documents (HR, benefits, IT)

## Note
Retrieval here is keyword-based. Next week's lab moves to vector embeddings for semantic search.
