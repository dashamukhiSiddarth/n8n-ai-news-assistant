# Personalized AI News Assistant (n8n)

A simple, self-hosted automation that delivers a clean daily news digest
directly to Telegram — without ads, subscriptions, or clutter.

This project was built to solve a real personal problem.

---

## **Why I Built This**

My father often complained about reading news on mobile apps and websites.
Most news platforms today are filled with:

- Too many third-party advertisements  
- Pop-ups and distractions  
- Paid subscriptions for basic access  
- Endless scrolling that makes reading tiring  

As a result, even reading simple daily news became frustrating for him.

So I decided to build a **simple solution**:
> A system that sends only the important news, directly from trusted sources,
summarized and delivered cleanly no ads, no noise, no subscriptions and also save money.

--->

## What This Project Does

Every morning, this automation:

- Fetches **top automobile-related news**
  - **3 local news articles**
  - **7 global news articles**
- Collects news **directly from newspapers via NewsAPI**
- Uses AI to **summarize each article into 1–2 easy-to-read sentences**
- Formats everything into a **clean, readable message**
- Sends the final news digest to **Telegram automatically**

The result is a short, distraction-free news update that can be read in minutes.

---

## Key Benefits

- No advertisements  
- No subscriptions  
- No login or apps required  
- Easy-to-read summaries  
- Delivered automatically every day  
Designed especially for non-technical users who just want the news.

---

## Tech Stack

- **n8n** – Workflow automation
- **Docker** – Local runtime environment
- **NewsAPI** – News source
- **Hugging Face Inference API** – AI-based summarization
- **Telegram Bot API** – Message delivery

---

## How It Works (High Level)

1. A **Cron trigger** runs every morning
2. News is fetched from NewsAPI (local + global)
3. Duplicate articles are removed
4. Each article is summarized using AI
5. A clean message is generated
6. The message is sent to Telegram automatically

---

## Run Locally

```bash
docker run -it --rm -p 5678:5678 -v ~/.n8n:/home/node/.n8n n8nio/n8n
