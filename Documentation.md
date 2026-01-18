Project Documentation
Personalized AI News Assistant (n8n)

1. Overview

The Personalized AI News Assistant is an automated system that delivers a clean, ad-free daily news digest directly to Telegram.
The system fetches automobile-related news from trusted sources, summarizes each article using AI, and sends a concise update every morning — without requiring subscriptions, logins, or mobile apps.

2. Problem Statement

Modern news applications often suffer from:
Excessive third-party advertisements
Pop-ups and distractions
Mandatory subscriptions
Poor reading experience for elderly users
For non-technical and retired users, reading online news becomes frustrating and time-consuming.
This project was created to simplify news consumption by removing unnecessary noise and focusing only on important information.

3. Solution Approach

The solution automates the entire news delivery process:
News is fetched directly from newspapers using official APIs
AI is used to summarize content into short, readable sentences
The final output is delivered as a simple text message on Telegram

This ensures:

No advertisements
No subscriptions
No application clutter

4. System Architecture

The system is built using a workflow-based automation approach.
High-Level Flow:
Scheduled trigger starts the workflow
News is fetched from multiple sources
Articles are cleaned and de-duplicated
AI generates summaries
A formatted message is created
Message is delivered to Telegram

5. Workflow Breakdown

5.1 Cron Trigger

Runs once every day (morning schedule)
Automatically starts the workflow

5.2 News Fetching

Uses NewsAPI
Fetches:
3 local automobile news articles
7 global automobile news articles

5.3 Data Cleaning

Removes duplicate articles
Extracts only useful fields:
Title
Description
Source
URL

5.4 AI Summarization

Uses Hugging Face Inference API
Converts long news content into:
1–2 simple sentences
Easy-to-read language
Optimized for non-technical readers

5.5 Message Formatting

Articles are grouped into:
Local news and Global news
Clean, readable text format
Includes source name and article link

5.6 Telegram Delivery

Uses Telegram Bot API
Sends a single formatted message
Delivered automatically every day

6. Technology Stack

Component	Purpose
n8n	Workflow automation
Docker	Local execution environment
NewsAPI	News data source
Hugging Face API	AI summarization
Telegram Bot API	Message delivery

7. Installation & Setup

Prerequisites
Docker installed
Free API keys:
NewsAPI
Hugging Face
Telegram Bot
Steps
Run n8n using Docker
Import the provided workflow.json
Add API credentials in n8n
Activate the workflow
Once active, the system runs automatically.

8. Security & Privacy

No API keys are stored in this repository
All credentials are securely managed inside n8n
Uses only official APIs
No scraping or paywall bypassing
No personal data storage

9. Limitations

Depends on free API rate limits
Requires Docker to be running
Summaries depend on AI model availability
These limitations are acceptable for personal and small-scale use.

10. Future Enhancements

WhatsApp integration (via official APIs)
Topic customization per user
Cloud deployment (24/7 uptime)
Multi-language news summaries
User preferences dashboard

11. Conclusion

This project demonstrates how automation and AI can be used to solve a real-world usability problem.
By focusing on simplicity and user experience, the system delivers value without complexity, subscriptions, or distractions.
It is a practical example of:
Workflow automation
API integration
AI-powered content processing
Building for real users

12. License
MIT License
