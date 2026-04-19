# 🤖 GitHub Auto-Documenter (n8n + Groq AI)

A high-performance, low-code automation tool that monitors your GitHub repository and uses **Groq-powered LLMs** to automatically generate professional documentation summaries.

---

## 🏗️ Workflow Architecture

This project is powered by an n8n workflow that connects GitHub's event system to Groq's ultra-fast Llama 3 models.

![n8n Workflow Screenshot](assets/workflow.png)

### ⚡ How it Works:
1. **GitHub Trigger:** Detects a `push` event in the repository.
2. **AI Agent (Groq):** Analyzes the commit messages and modified files using **Llama-3.3-70B**.
3. **GitHub Writer:** Automatically updates this README with a professional summary of the changes.

---

## 🛠️ Tech Stack

| Tool | Purpose |
| :--- | :--- |
| **n8n** | Workflow Orchestration & Logic |
| **Groq** | Ultra-fast LLM Inference (Llama 3.3-70B) |
| **GitHub API** | Version Control & Webhook Trigger |
| **Markdown** | Dynamic Documentation Formatting |

---

## 🔧 Installation & Setup

1. **n8n Configuration:**
   - Import the provided JSON workflow.
   - Set up your **Groq API Key** and GitHub **Personal Access Token**.
2. **Webhook Setup:**
   - Point your GitHub repository Webhook to your n8n Production URL.
   - Set Content-type to `application/json`.
3. **Enjoy Automation:**
   - Every push will now trigger an automatic documentation update.

---

## 📜 Automated Changelog
*This section is managed by the Auto-Documenter AI. New updates will appear below.*