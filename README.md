# 🚀 Integrating MCP Memory into an AI Agent

This project demonstrates how to build an AI agent that supports **web search**, **persistent memory**, and **observability**, fully powered by open-source MCP (Model Context Protocol) tools.

---

## 🧰 Tech Stack

- **[CrewAI](https://github.com/crewAIInc)** — Framework for building MCP-compatible agents  
- **[Zep Graphiti](https://github.com/getzep/graphiti)** — Human-like long-term memory  
- **[CometML Opik](https://github.com/comet-ml/opik)** — Tracing, monitoring & observability  
- **100% Open-Source**

---

## 🧠 System Overview

The system runs through the following pipeline:

1. User submits a query  
2. Agent performs an MCP-powered web search  
3. Query + search results are sent to the Memory Manager  
4. Memory Manager stores relevant context inside **Graphiti**  
5. Response Agent uses memory + search results to generate the final answer  

---

# ⚙️ Setup Guide

## 1. Install & Configure Ollama

### Install Ollama

**macOS:**
```bash
curl -fsSL https://ollama.com/install.sh | sh
````

**Linux:**

```bash
curl -fsSL https://ollama.com/install.sh | sh
```

**Windows:**
Download the installer from:
[https://ollama.com/download](https://ollama.com/download)

### Pull the required model

```bash
ollama pull llama3.2
```

Ensure Ollama is running before continuing.

---

## 2. Add Environment Variables

Create your `.env` file from the provided template:

```bash
cp .env.example .env
```

Open `.env` and fill in your API keys (Linkup, Opik, Graphiti, etc.).

---

## 3. Install Dependencies

Install all required dependencies using **uv**:

```bash
uv sync
```

---

# ▶️ Running MCP Servers

## 1. Start the Linkup MCP Server

1. Get your Linkup API keys: [https://www.linkup.so/](https://www.linkup.so/)
2. Start the server:

```bash
python server.py
```

---

## 2. Start the Graphiti MCP Server *(Optional but Recommended)*

Graphiti enables long-term memory support.

