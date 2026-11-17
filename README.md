# 🤖 AI Content Summarizer & Email Notifier

An automated workflow built with **n8n**, **Google Forms**, **Google Apps Script**, and **Google Gemini AI** that summarizes submitted articles and emails the summary directly to the user.

## ⚙️ How It Works
1. **Google Form:** Collects the article text and the user's email address.
2. **Google Apps Script:** Triggers on form submission and sends the data via a POST request to an n8n Webhook (tunneled locally via **ngrok**).
3. **n8n & Google Gemini AI:** Processes the text using an AI Agent node to generate a clean, bulleted summary.
4. **SMTP Email Node:** Automatically sends the generated summary to the user's inbox.

## 🛠️ Tech Stack
* **Workflow Automation:** n8n (Self-hosted / Local)
* **AI Model:** Google Gemini Chat Model
* **Trigger & Integration:** Google Forms + Google Apps Script
* **Tunneling:** ngrok

## 🚀 Setup Instructions
1. Import `workflow.json` into your n8n instance.
2. Configure your **Google Gemini API** credentials and **SMTP** credentials in n8n.
3. Create a Google Form with two fields: *Text/Article* and *Email Address*.
4. Open **Apps Script** from the Google Form, paste the code from `Code.gs`, and replace the webhook URL with your n8n Webhook URL.
5. Set up an `On form submit` trigger in Apps Script and test the workflow!

## 🎥 Live Demo

https://github.com/user-attachments/assets/24862a97-f264-4f57-a765-fe68a01f8d25

