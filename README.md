<img width="355" height="142" alt="download" src="https://github.com/user-attachments/assets/a1d4d2c5-6d9d-44c4-93d9-0a95280a47f9" />

 # 🤖 n8n Sonic AI Assistant

An **AI-powered personal assistant** built using **n8n**, **LangChain Agents**, **OpenAI / OpenRouter**, and **Telegram**, designed to manage your emails, calendar, tasks, and daily queries using voice or text conversations  all from a single chat interface.

This repository contains a fully modular n8n workflow that turns Telegram into a voice-enabled AI control center for your digital life.

---

## 🚀 Features

- 🎙️ Voice + Text interaction via Telegram  
- 🤖 AI Agent powered by LangChain  
- 🧠 Memory-enabled conversations (context-aware replies)  
- 📧 Read & send emails using Gmail  
- 📅 Fetch calendar events from Google Calendar  
- ✅ Create & retrieve tasks from Google Tasks  
- 🔁 Smart intent detection (voice vs text)  
- ⚡ Real-time responses directly in Telegram  
- 🔐 Secure OAuth-based integrations  

---

## 🧠 System Architecture

```text
Telegram (Voice / Text)
        ↓
Telegram Trigger (n8n)
        ↓
Voice/Text Detection Logic
        ↓
Speech-to-Text (OpenAI)
        ↓
AI Agent (LangChain + LLM + Memory)
        ↓
Google Tools (Gmail / Calendar / Tasks)
        ↓
Telegram Response
```


## 🔄 Workflow Overview
<img width="1695" height="802" alt="image" src="https://github.com/user-attachments/assets/f1e8352f-88ff-424d-92aa-2f4a164f737f" />


### 💬 Sonic AI Assistant (Telegram-Based)

This workflow acts as a **personal AI assistant** that understands **natural language commands** and executes actions across your Google ecosystem.

---

### 🔧 How It Works

- Triggered by **Telegram messages**
- Accepts:
  - 📝 Text messages
  - 🎤 Voice messages
- Automatically detects input type:
  - **Voice** → transcribed using OpenAI
  - **Text** → passed directly to the AI
- The **AI Agent**:
  - Understands user intent
  - Uses memory to stay context-aware
  - Calls tools such as:
    - Gmail
    - Google Calendar
    - Google Tasks
- Sends a **formatted response back to Telegram**

---

## 💬 Example Commands

- “What emails do I have today?”
- “Show my calendar for tomorrow”
- “Create a new to do item”
- “Send an email to John about the meeting”
- 🎤 Send a voice note for hands free control

---

## 🧠 AI Capabilities

- Intent detection (email, calendar, task, general query)
- Contextual follow ups using memory buffer
- Safe tool usage via LangChain agent
- Automatic parameter extraction from natural language

---

## 🛠️ Tech Stack

- **n8n** – Workflow orchestration  
- **Telegram Bot API** – User interaction layer  
- **LangChain (n8n nodes)** – Agent, tools, and memory  
- **OpenAI / OpenRouter** – LLM & voice transcription  
- **Google Gmail API** – Email access  
- **Google Calendar API** – Calendar management  
- **Google Tasks API** – Task management  

---

## ⚙️ Setup Instructions

### 1️⃣ Prerequisites

- n8n (Desktop, Docker, or Cloud)
- Telegram account
- Google account
- API keys for:
  - OpenAI **or** OpenRouter

---

### 2️⃣ Create Telegram Bot

1. Open Telegram → `@BotFather`
2. Create a new bot
3. Copy the **Bot Token**

---

### 3️⃣ Import Workflow

1. Open n8n  
2. Click **Import Workflow**  
3. Upload:


### 4️⃣ Configure Credentials in n8n

Add the following credentials:

- **Telegram API** (Bot Token)
- **OpenAI API** or **OpenRouter API**
- **Gmail OAuth2**
- **Google Calendar OAuth2**
- **Google Tasks OAuth2**

---

### 5️⃣ Activate Workflow

⚠️ **Telegram requires HTTPS webhooks**

Choose one:

- Use **ngrok** for local development  
- Or deploy **n8n on a cloud server**

Once active:

- Send a message or voice note to your bot  
- Your **Sonic AI Assistant is live** 🚀

---

## 🔐 Notes & Limitations

- Only **one Telegram trigger per bot** is allowed
- Workflow requires **HTTPS** for activation
- Voice transcription uses **OpenAI credits**
- Memory uses **session-based Telegram chat IDs**

---

## 🎯 Use Cases

- Personal productivity assistant
- Voice controlled task manager
- Email & calendar automation
- AI powered daily planner

