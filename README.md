# 🚀 Agentic GitHub Workflow using CrewAI + MCP + Django

An end-to-end AI-powered GitHub automation system that uses CrewAI agents, GitHub MCP (Model Context Protocol), and Django to analyze repositories, generate structured documentation, and produce intelligent reports.

This project demonstrates how multiple specialized AI agents can collaborate to understand and summarize GitHub repositories in a production-style web workflow.

---

## 🧠 What This Project Does

Given a GitHub repository URL, the system:

1. 📂 Scans repository structure
2. 🧾 Lists and summarizes issues
3. 🔀 Retrieves recent pull requests
4. 🌿 Lists repository branches
5. 📄 Generates Markdown documentation
6. 🌐 Converts Markdown to HTML for display in a Django interface

All of this is orchestrated through CrewAI multi-agent collaboration.

---

## 🏗️ Architecture Overview

User Input (GitHub URL)
↓
Django Web Interface
↓
CrewAI Orchestration
↓
Specialized Agents
↓
MCP GitHub Server
↓
Generated Markdown Reports
↓
HTML Rendering


---

## 🤖 AI Agents

### 1️⃣ Repository Structure Auditor
- Uses `get_repo_files` tool
- Generates Markdown-based file tree
- Creates clickable links to GitHub files

### 2️⃣ GitHub Issue Analyst
- Retrieves open issues
- Summarizes and prioritizes issues

### 3️⃣ Pull Request Reporter
- Fetches latest pull requests
- Generates concise report

### 4️⃣ Branch Reporter
- Lists repository branches
- Produces structured output

---

## 🛠️ Tech Stack

- **Python 3.11**
- **Django**
- **CrewAI**
- **LangChain**
- **OpenAI API**
- **GitHub MCP Server**
- **Markdown → HTML conversion**

---

## 📁 Project Structure

mcp_integration/
│
├── mcp_manager/
│ ├── agents/
│ ├── tasks/
│ ├── tools/
│ ├── templates/
│ └── views.py
│
├── generated_docs/
├── manage.py
└── settings.py


---
EXAMPLE:
<img width="2157" height="1584" alt="image" src="https://github.com/user-attachments/assets/b0e33418-fefd-4400-a354-25a276c85443" />
<img width="2306" height="1500" alt="image" src="https://github.com/user-attachments/assets/b58d431d-0df3-4862-aad9-bf97c4fab91f" />


## ⚙️ Setup Instructions

### 1️⃣ Clone Repository

```bash
git clone https://github.com/nehayargal/Agentic_workflow_GitHub_MCP.git
cd Agentic_workflow_GitHub_MCP
2️⃣ Create Virtual Environment
python -m venv venv
source venv/bin/activate
3️⃣ Install Dependencies
pip install -r requirements.txt
4️⃣ Configure Environment Variables
Create a .env file:

OPENAI_API_KEY=your_openai_api_key
GITHUB_PERSONAL_ACCESS_TOKEN=your_github_token
OR export directly:

export OPENAI_API_KEY=your_key
export GITHUB_PERSONAL_ACCESS_TOKEN=your_token
5️⃣ Run Server
python manage.py runserver
Visit:

http://localhost:8000
🔐 Security Note
Secrets are loaded using environment variables and are not stored in the repository.

🧩 Key Engineering Highlights
Multi-agent orchestration using CrewAI

StructuredTool integration for GitHub MCP interaction

Dynamic Markdown file aggregation

Runtime Markdown-to-HTML rendering

Django-based UI integration

Environment-driven secure configuration

Modular tool architecture for extensibility

📈 Potential Extensions
Add repo summarization via embeddings

Generate architectural diagrams

Add contributor analytics

Deploy to cloud (Render / AWS)

Add caching layer

Implement async task execution

🎯 Why This Project Matters
This project demonstrates:

Agentic AI system design

Production-style web integration

Secure API handling

Multi-tool LLM orchestration

GitHub automation via MCP

Clean modular backend architecture

👩‍💻 Author
Neha Yargal

Senior Software Engineer
AI +  Distributed Systems
