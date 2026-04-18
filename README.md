# 🤖 Auto-Documenter (n8n + Groq)

An automated workflow that monitors GitHub pushes and uses **Groq LLMs** to generate instant documentation summaries.

## 🚀 How it Works
1. **Trigger:** GitHub Webhook fires on a `push` event.
2. **Analysis:** n8n fetches the commit diff.
3. **AI Processing:** Groq (Llama 3) analyzes the code changes.
4. **Output:** A summarized changelog is posted to Slack/Discord or updated in a `CHANGELOG.md`.

## 🛠️ Setup
1. Import the JSON file from `/workflows` into your n8n instance.
2. Set up your **Groq API Key** in the OpenAI Chat Node (Base URL: `https://api.groq.com/openai/v1`).
3. Connect your GitHub Webhook.

## 📦 Tech Stack
- **n8n** (Orchestration)
- **Groq** (Inference Engine)
- **GitHub API**