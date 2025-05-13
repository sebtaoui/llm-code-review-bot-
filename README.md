# 🤖 LLM-Code-Review-Bot

An open-source GitHub-integrated code review assistant powered by local LLMs like [StarCoder](https://huggingface.co/bigcode/starcoder) or [Code LLaMA](https://huggingface.co/codellama). This bot automatically analyzes pull request diffs and provides feedback on code quality, security issues, and improvement suggestions — all without relying on external APIs.

---

## 🧠 Features

- Analyze code changes in real-time on pull requests
- Run open-source LLMs locally using HuggingFace Transformers
- Post review suggestions as GitHub comments
- Fully offline-compatible (no OpenAI or cloud services required)
- Containerized with Docker for easy deployment

---

## 🚀 Tech Stack

- **Python** & **FastAPI** — for API and webhook handling  
- **GitHub API** — for PR and diff access  
- **HuggingFace Transformers** — to load StarCoder or Code LLaMA  
- **Docker** — to package and deploy the app  
- **Gunicorn + Uvicorn** — for production server

---

## ⚙️ Installation

```bash
git clone https://github.com/sebtaoui/llm-code-review-bot.git
cd llm-code-review-bot
docker build -t llm-code-review-bot .
docker run -d -p 8000:8000 llm-code-review-bot
