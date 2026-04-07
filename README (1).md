# NebulaFlow Risk Management Agent: 2026 Supply Chain Demo

## Project Overview
This project demonstrates a next-generation **Agentic RAG (Retrieval-Augmented Generation)** system designed for high-stakes risk management in procurement and supply chain. Using a fictional 2026 business landscape, the agent analyzes global macroeconomic trends against internal company data to perform real-world actions.

## 🏢 Mock Company: NebulaFlow Systems Inc.
- **Industry:** Automated Logistics & AI-Enabled Edge Computing.
- **Product:** *FlowNodes* (Hardware bridging AI agents to physical warehouses).
- **Core Challenge:** Navigating the "End of Cheap Scale" and "Regulatory Whiplash" of 2026.

## 🛠️ System Architecture
The application is built on five core pillars:
1. **RAG (Knowledge):** Ingests and retrieves context from the **GEP 2026 Outlook** and **WTO March 2026 Trade Reports**.
2. **Relational Data (SQL):** Manages structured internal data including suppliers (India, Mexico, Vietnam), contracts, and inventory.
3. **MCP (Model Context Protocol):** Securely bridges the LLM to local resources (PDFs and CSVs) without cloud-side data exposure.
4. **Agent Logic (Reasoning):** A ReAct loop that determines when to read a report versus when to query a database.
5. **Actions (REST/Tools):** Live capability to simulate market price checks (e.g., $90/bbl oil) and trigger supplier audits via REST APIs.

## 📂 Included Demo Files
- `NebulaFlow_Systems_10K_2026.pdf`: A pro-forma SEC filing detailing company financials, regional growth (7.0% in India), and 19.5% tariff risks.
- `NebulaFlow_Corporate_Profile.pdf`: A strategic overview of the company's mission and "Resilience-as-a-Value" pillars.
- `Global_Outlook_March_2026_Procurement_And_Supply_Change.pdf`: The primary knowledge base for the agent.

## 🚀 GitHub Copilot Implementation Prompts

### 1. Database Initialization
```text
"Create a SQLAlchemy script to initialize a PostgreSQL DB for NebulaFlow with tables for Suppliers, Contracts, and Macro_Stats. Seed it with mock 2026 data."
```

### 2. RAG Pipeline
```text
"Build a RAG pipeline using LangChain and Vertex AI to embed the NebulaFlow 10-K and GEP Outlook PDFs into a FAISS vector store."
```

### 3. MCP Server Setup
```text
"Implement a Python MCP server using the mcp SDK to expose local risk-assessment tools and CSV resources to a Gemini agent."
```

### 4. Agentic Actions
```text
"Define tool-calling functions for 'trigger_supplier_audit' (REST POST call) and 'get_market_oil_price' (REST GET call) for a risk management agent."
```

## 📈 Demo Scenarios
- **Scenario A:** User asks about tariff impact. Agent reads WTO report (19.5% rate), queries SQL (Gujarat supplier exposure), and suggests a price hike simulation.
- **Scenario B:** User asks about energy costs. Agent reads GEP report ($90/bbl forecast), calls the REST API for live rates, and flags European logistics contracts.
- **Scenario C:** User asks about compliance. Agent identifies "Regulatory Whiplash" in the PDF and uses the MCP server to check local supplier certificates.

---
*Created for the 2026 Supply Chain Risk Management Demo.*
