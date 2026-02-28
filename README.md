# AI Personal Assistant Ecosystem (n8n + Telegram)

This project contains a series of **n8n workflows** designed to transform a Telegram bot into a powerful AI Personal Assistant. By leveraging LangChain AI Agents and OpenAI, these workflows allow you to manage your digital life—emails, calendar, and general tasks—directly through a chat interface.

---

## 🚀 Workflows Overview

The project is split into three evolving stages of complexity:

### 1. Basic Telegram Bot (`Workflow 2`)

The foundational setup. It connects a Telegram bot to an OpenAI Chat Model, allowing for natural language conversations.

* **Key Features:** Simple chat interface, AI-driven responses.
* **Nodes:** Telegram Trigger → AI Agent (GPT-5 Mini) → Telegram Send Message.

### 2. E-mail Integrated Agent (`Workflow 3`)

Adds "eyes" to your inbox. The AI agent is equipped with a **Gmail Tool**, enabling it to fetch and read your emails upon request.

* **Key Features:** Can search and retrieve your latest Gmail messages via Telegram commands.
* **Tools:** Gmail "Get Many Messages" tool.

### 3. Full Productivity Suite (`Workflow 1`)

The most advanced version. It combines email access with **Google Calendar** integration, creating a true virtual assistant.

* **Key Features:** Read emails and check your schedule in one place.
* **Tools:** Gmail Tool + Google Calendar "Get Event" tool.

---

## 🛠️ Tech Stack

* **Automation:** [n8n](https://n8n.io/)
* **Orchestration:** LangChain (AI Agent)
* **AI Model:** OpenAI (GPT-5 Mini)
* **Interface:** Telegram Bot API
* **Integrations:** Gmail API, Google Calendar API

---

## ⚙️ Setup Instructions

### 1. Prerequisites

* An **n8n** instance (self-hosted or cloud).
* A **Telegram Bot Token** (obtainable via [@BotFather](https://t.me/botfather)).
* **OpenAI API Key**.
* **Google Cloud Console** credentials (OAuth2) for Gmail and Calendar access.

### 2. Installation

1. Download the `.json` workflow files from this repository.
2. In n8n, click **Import from File** and select the desired workflow.
3. Configure your credentials:
* **Telegram API:** Input your Bot Token.
* **OpenAI API:** Input your API Key.
* **Gmail/Google Calendar OAuth2:** Follow the n8n OAuth2 setup guide to link your Google account.



### 3. Activation

* Ensure the **Webhook URLs** are correctly registered by toggling the workflow to **Active**.
* For the Telegram Trigger, ensure your bot is not in "Privacy Mode" if you want it to respond in groups, or simply message it directly.

---

## 📖 Usage Examples

* **General:** "What is the capital of France?"
* **Email:** "Check my last 5 emails and summarize if there are any urgent tasks."
* **Calendar:** "What do I have scheduled for today at 2 PM?"

---

## ⚠️ Notes

* **GPT-5 Mini:** Ensure your OpenAI account has access to the model specified in the JSON, or swap it for `gpt-4o` or `gpt-3.5-turbo` in the **OpenAI Chat Model** node settings.
* **Security:** These workflows allow an AI to read your private data. Ensure your n8n instance is secured and your Telegram bot is not shared publicly without restriction.

---

