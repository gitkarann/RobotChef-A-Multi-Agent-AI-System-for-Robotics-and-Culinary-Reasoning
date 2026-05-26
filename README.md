
# 🚀 From Prompts to Agents — AI Systems Engineering Playground

A modular framework for building and experimenting with **LLM-powered agents, tool-using systems, RAG pipelines, and multi-agent architectures**.

This project explores how modern AI agent systems are designed and implemented in practice.

---

# 🧠 System Overview

This repository demonstrates:

- LLM-based chat systems
- Tool-using agents (MCP-style architecture)
- Retrieval-Augmented Generation (RAG)
- Multi-agent workflows
- Prompt engineering experiments
- Streamlit-based AI applications

---

# 🏗️ Architecture

## High-Level System Design

```
User Interface (CLI / Streamlit)
            ↓
     Agent Controller
            ↓
 ┌──────────┼──────────┐
 ↓          ↓          ↓
LLM     Tool Layer   RAG System
Backend  (MCP Tools)  (Vector DB)
            ↓
     Execution Layer
            ↓
      Final Response
```

---

# ⚙️ How It Works

The system follows a **Reason → Act → Observe → Respond loop**:

1. **Input**
   - User submits query via CLI or Streamlit UI

2. **Reasoning (LLM)**
   - Determines whether tools or retrieval are needed

3. **Action (Tool Use)**
   - Executes MCP tools, APIs, or functions if required

4. **Observation**
   - Tool outputs are returned to the LLM

5. **Final Response**
   - LLM synthesizes final answer

---

# 🤖 Agent Flow

## Tool-Using Agent (Session 2)

```
User
 ↓
LLM Planner
 ↓
Tool Selection
 ↓
External Tool Execution
 ↓
Observation
 ↓
Final Response
```

## RAG Pipeline (Session 3)

```
User Query
 ↓
Embedding Search
 ↓
Vector Retrieval
 ↓
Context Injection
 ↓
LLM Answer
```

## Multi-Agent System (Session 5)

```
Agent A (Planner)
        ↓
   Coordinator
        ↓
Agent B   Agent C   Agent D
(tool)    (critic)  (executor)
```

---

# 📁 Project Structure

```
session1 → LLM chat + prompt engineering
session2 → Tool-using agent (MCP)
session3 → RAG system
session4 → Recipe/tool agent
session5 → Multi-agent system (A2A)
```

---

# ⚡ Setup

## 1. Clone repository

```bash
git clone https://github.com/UH-Workshop-M726/FromPromptsToAgents.git
cd FromPromptsToAgents
```

## 2. Create environment

```bash
python -m venv .venv

# Windows
.venv\Scripts\activate

# Linux / macOS
source .venv/bin/activate
```

---

# 🔌 LLM Backend Setup

## Option A — University LLM

```env
LLM_SERVICE_URL=https://uhhpc.herts.ac.uk/qwen
LLM_API_TOKEN=your_token_here
```

## Option B — Google Gemini

1. Get API key: https://aistudio.google.com  
2. Add to `.env`:

```env
GEMINI_API_KEY=your_key_here
```

---

# ▶️ Running the Project

## Session 1
```bash
cd session1
pip install -r requirements.txt
python steps/step1_hello_llm.py
streamlit run steps/step4_chatbot.py
```

## Session 2
```bash
cd session2
python steps/step3_run_agent.py
```

## Session 3
```bash
cd session3
streamlit run rag_streamlit.py
```

## Session 4
```bash
cd session4
python steps/step3_run_agent.py
```

## Session 5
```bash
cd session5
streamlit run app.py
```

---

# 📊 Conceptual Benchmarks

| System Type        | Accuracy | Tool Use | Hallucination Rate |
|-------------------|----------|----------|---------------------|
| Raw LLM           | Medium   | None     | High                |
| Tool-Augmented    | High     | Yes      | Medium              |
| RAG System        | High     | Yes      | Low                 |
| Multi-Agent System| Very High| Advanced | Lowest              |

---

# 📸 Outputs

Include screenshots here:

```
/screenshots/chatbot.png
/screenshots/agent.png
/screenshots/rag.png
```

Example:

```md
![Chatbot UI](screenshots/chatbot.png)
```

---

# 🧠 Key Design Principles

- Modular architecture (session-based design)
- Swappable LLM backends
- Tool-first agent design
- Separation of reasoning vs execution
- Experimental RAG + multi-agent systems

---

# ⚠️ Limitations

- Requires API keys or local LLM backend
- Not production-optimized
- RAG system is educational
- Benchmarks are conceptual unless measured

---

# 🚀 Future Improvements

- Persistent memory system
- Production-grade vector database
- Real-time streaming agents
- Distributed multi-agent execution
- Evaluation framework for agents

---

# 🧩 Summary

This project demonstrates how to move from:

**basic prompts → structured AI agents → tool-using systems → multi-agent architectures**

It is a learning + experimentation framework for modern AI system design.
