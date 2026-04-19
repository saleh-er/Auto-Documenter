# 🤖 GitHub Auto-Documenter (n8n + Groq AI)

A high-performance, low-code automation tool that monitors your GitHub repository and uses **Groq-powered LLMs** (Llama 3) to automatically generate professional changelogs and documentation summaries.

---

## 🚀 Overview

This project solves the "lazy developer" problem by automating the most tedious part of coding: **Documentation**. By bridging GitHub Webhooks with n8n and Groq's ultra-fast inference engine, every code push is analyzed and summarized in real-time.

### ⚡ Key Features
- **Real-time Monitoring:** Uses GitHub Webhooks to trigger on every `push` event.
- **AI-Powered Analysis:** Leverages **Groq (Llama 3)** to understand code diffs and commit messages.
- **Self-Documenting:** Automatically updates the `README.md` or `CHANGELOG.md` with structured summaries.
- **[skip ci] Integration:** Built-in logic to prevent infinite automation loops.

---

## 🛠️ Tech Stack

| Tool | Purpose |
| :--- | :--- |
| **n8n** | Workflow Orchestration & Logic |
| **Groq** | Ultra-fast LLM Inference (Llama 3.3-70B) |
| **GitHub API** | Version Control & Webhook Trigger |
| **Markdown** | Dynamic Documentation Formatting |

---

## 🏗️ Workflow Architecture

1. **The Trigger:** GitHub sends a POST request (Webhook) to n8n containing commit data.
2. **The Brain:** n8n sends the commit message and file list to the **Groq API**.
3. **The Writer:** n8n receives the AI summary and uses the GitHub node to update the repository files.

---

## 🔧 Installation & Setup

### 1. Prerequisites
- An **n8n** instance (Desktop, Docker, or Cloud).
- A **Groq API Key** (Get it at [console.groq.com](https://console.groq.com)).
- A GitHub **Personal Access Token (PAT)** with `repo` permissions.

### 2. n8n Configuration
1. Import the `workflows/auto-documenter.json` file into n8n.
2. Configure the **OpenAI Chat Model** node:
   - **Base URL:** `https://api.groq.com/openai/v1`
   - **API Key:** Your Groq Key.
   - **Model:** `llama-3.3-70b-versatile`.
3. Set your GitHub credentials in the **GitHub Trigger** and **GitHub** nodes.

### 3. Repository Setup
1. Add a Webhook in your GitHub repo settings pointing to your n8n production URL.
2. Ensure your `README.md` has a section for the AI to write to.

---

## 📜 Automated Changelog
*This section is managed by the Auto-Documenter AI.*

------

## 🤝 Contributing
Feel free to fork this project and add features like **Slack/Discord notifications** or **Automatic Release notes**!

## 📄 License
MIT License - created by [Your Name/GitHub Username]