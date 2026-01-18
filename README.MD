# Personalized AI News Assistant (n8n)

A self-hosted AI automation that delivers a clean daily automobile news digest
directly to Telegram every morning.

Built as a real-world project to help a retired parent consume news without ads,
noise, or information overload.
--
## 🚗 Features
- Fetches 3 local + 7 global automobile news articles
- AI-powered 1–2 sentence summaries
- Clean Telegram delivery
- Fully automated with Cron
---
## 🛠 Tech Stack
- n8n
- Docker
- NewsAPI
- Hugging Face Inference API
- Telegram Bot API
---
## ⚙️ How It Works
Cron → NewsAPI → AI Summarization → Formatter → Telegram
---
## ▶️ Run Locally
```bash
docker run -it --rm -p 5678:5678 -v ~/.n8n:/home/node/.n8n n8nio/n8n
