# AI-Powered Investment Risk Intelligence Platform (RAG + MCP + Agentic AI)

## Overview

This project demonstrates a realistic AI system inspired by BlackRock
Aladdin platform capabilities. It combines:

-   RAG (Retrieval Augmented Generation)
-   MCP Tool Calling
-   Agentic AI workflows
-   Streamlit UI
-   Redis Vector Database

The application allows users to upload financial documents and portfolio
allocations and interact with an AI agent that performs risk analysis
and compliance checks.

------------------------------------------------------------------------

# Tech Stack

-   Python 3.11+
-   Streamlit
-   LangChain or LlamaIndex
-   OpenAI API (or local LLM)
-   Redis Vector Database
-   Pandas
-   Plotly
-   FastAPI (optional)
-   Docker

------------------------------------------------------------------------

# Architecture

User → Streamlit UI → AI Agent → MCP Tools → Redis Vector DB → Financial
Documents

------------------------------------------------------------------------

# Features

## 1. Document Ingestion (RAG)

Supported formats: - PDF - TXT - CSV - HTML

Steps: 1. extract text 2. split text into chunks 3. generate embeddings
4. store embeddings in Redis vector database 5. semantic search

Embedding model: text-embedding-3-small

------------------------------------------------------------------------

## 2. Portfolio Input

Example CSV:

Asset,Weight AAPL,20 MSFT,15 TSLA,10 Bond ETF,40 Gold ETF,15

Visualizations: - allocation pie chart - diversification score - asset
category distribution

------------------------------------------------------------------------

## 3. AI Agent Workflow

The AI agent can: - retrieve knowledge using RAG - call tools when
needed - simulate market scenarios - detect compliance violations

Example queries:

What are major risks in my portfolio? How will interest rate increase
affect my portfolio? Check compliance violations Simulate recession
impact

------------------------------------------------------------------------

## 4. MCP Tools

### Tool 1 --- portfolio_risk_tool

Input: portfolio dataframe

Output:

risk_score equity exposure bond exposure diversification score

------------------------------------------------------------------------

### Tool 2 --- stress_test_tool

Scenarios:

recession inflation spike interest rate hike oil shock

Output:

expected drawdown percentage

------------------------------------------------------------------------

### Tool 3 --- compliance_tool

Rules:

crypto exposure \< 5% single stock exposure \< 25% emerging market
exposure \< 30%

Detect violations.

------------------------------------------------------------------------

### Tool 4 --- market_sentiment_tool

Analyze financial news sentiment.

Output:

sentiment score risk level explanation

------------------------------------------------------------------------

## 5. Streamlit UI

### Page 1

Upload documents

### Page 2

Upload portfolio CSV

### Page 3

AI chat interface

Example questions:

simulate market crash summarize risk factors top portfolio risks

------------------------------------------------------------------------

## 6. Vector Search

Store:

embedding text chunk metadata

Use Redis vector database.

------------------------------------------------------------------------

## 7. Output Format

Risk Summary:

Top Risks: 1. 2. 3.

Recommendations: 1. 2.

Confidence Score: %

------------------------------------------------------------------------

# Folder Structure

app.py

rag/ document_loader.py embedding.py vector_store.py

agent/ agent.py tools.py prompts.py

ui/ pages/

data/

------------------------------------------------------------------------

# Docker Support

docker-compose services:

redis app

------------------------------------------------------------------------

# Sample Prompt Template

You are financial risk analyst AI.

Always:

use retrieved knowledge call tools when needed provide structured output
highlight risk factors

------------------------------------------------------------------------

# Demo Flow

1.  upload portfolio csv
2.  upload financial document
3.  ask questions
4.  simulate recession
5.  show charts

------------------------------------------------------------------------

# Run Application

streamlit run app.py

------------------------------------------------------------------------
