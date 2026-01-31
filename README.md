# 🧠 Personal Life Manager AI  
### Telegram + Google Services + Voice-Enabled AI using n8n

An AI-powered personal assistant built using **n8n** that connects **Telegram**, **voice input**, and **Google services (Gmail, Calendar, Tasks)** to manage daily activities using natural language.

This project demonstrates an AI agent workflow with real integrations and tool calling.

Workflow: 
<img width="935" height="431" alt="Screenshot 2026-01-31 130937" src="https://github.com/user-attachments/assets/6d2351fb-a05a-46e3-a2ea-7d9c07cea523" />

Output:
<img width="945" height="434" alt="Screenshot 2026-01-31 131753" src="https://github.com/user-attachments/assets/98aad808-3514-4955-a79d-b1ab7555790b" />

<img width="319" height="128" alt="image" src="https://github.com/user-attachments/assets/37c1e4c6-cf02-4b7b-bb49-db73f4200408" />

Full demo:
https://drive.google.com/file/d/1RNbIeXZyUWTNDKl4I9fYBMauYefUI_-Z/view?usp=sharing

## 🚀 Features

- Telegram chatbot interface
- Voice and text input support
- Automatic voice transcription
- AI assistant with short-term memory
- Google Tasks integration
- Gmail read and send support
- Google Calendar availability check
- Modular AI tool-calling workflow
- No-code orchestration using n8n

---

## 🧩 Workflow Overview

Telegram message / voice
↓
Detect voice or text
↓
Download voice file (if any)
↓
Transcribe voice to text
↓
AI Agent (LLM + Memory + Tools)
↓
Google / Gmail / Calendar actions
↓
Reply back to Telegram


---

## 🛠 Main Nodes Used

| Node | Purpose |
|-----|------|
| Telegram Trigger | Listens for incoming Telegram messages |
| Voice or Text Switch | Detects whether the message is voice or text |
| Telegram – Get File | Downloads voice file |
| Transcription Node | Converts voice to text |
| AI Agent | Main reasoning and tool selection |
| Window Buffer Memory | Keeps recent conversation context |
| Google Tasks | Create and read tasks |
| Gmail | Read and send emails |
| Google Calendar | Check availability |
| Telegram Send Message | Sends response back to user |

---

## 🤖 AI Capabilities

The assistant can:

- create tasks
- fetch existing tasks
- read emails
- send emails
- check calendar availability
- answer general questions

The AI agent automatically selects the required tool based on the user message.

---

## 🎤 Voice Support

Users can send a voice message from Telegram.

The workflow automatically:

1. downloads the audio
2. transcribes it
3. sends the text to the AI agent

---

## 🧠 Memory Support

A **Window Buffer Memory** node is used to store recent conversation messages so the assistant can respond in a more contextual and natural way.

---

## 🔐 Required Credentials

Configure the following credentials in n8n:

- Telegram Bot API
- OpenAI or OpenRouter API (chat + transcription)
- Google OAuth2 (Gmail, Calendar, Tasks)

---

## ⚙ Setup Instructions

### 1. Import workflow

Import the provided n8n workflow JSON file into your n8n instance.

---

### 2. Create Telegram bot

- Create a bot using **@BotFather**
- Copy the bot token
- Configure it in the Telegram nodes

---

### 3. Configure AI model

Set your OpenAI or OpenRouter API key inside the AI Chat Model node.

---

### 4. Connect Google services

Authorize:

- Gmail
- Google Calendar
- Google Tasks

using Google OAuth credentials.

---

### 5. Activate the workflow

Click **Activate** in n8n.

Your personal AI assistant is now live.

---

## 📸 Workflow Screenshot

![Workflow](./Screenshot-Workflow.png)

Upload your workflow image and name it `Screenshot-Workflow.png`.

---


## 💡 Why this project is important

This project demonstrates:

- AI agent orchestration
- tool calling using LLMs
- voice and text multimodal interaction
- real-world API integrations
- no-code AI automation architecture

---

## 🧑‍💻 Author

Rohit Bachchhe  
AI & Data Science Engineer  
n8n | LLM Agents | Automation | Analytics

---

## 🏷 Tech Stack

- n8n
- Telegram Bot API
- OpenAI / OpenRouter
- Google Gmail API
- Google Calendar API
- Google Tasks API
- Speech-to-Text model
