# 🧠 End-to-End NLP Chatbot for Food Delivery

An intelligent food ordering chatbot built using **Dialogflow**, **FastAPI**, and **MySQL**, complete with a static website frontend and backend integration. The bot helps users place and track food delivery orders through natural language.

---

## 📁 Directory Structure

```
├── backend/               # FastAPI backend code
├── db/                    # MySQL dump (import using Workbench)
├── dialogflow_assets/     # Intents, training phrases, entities etc.
└── frontend/              # Static website frontend code
```

---

## 🚀 Tech Stack

| Technology      | Description                        |
|-----------------|------------------------------------|
| 🐍 Python        | Core programming language           |
| ⚡ FastAPI       | Web framework for backend APIs      |
| 🐬 MySQL         | Relational database                 |
| 🤖 Dialogflow    | Conversational AI platform          |
| 🌐 Ngrok         | HTTPS tunneling for webhook         |
| 🌐 HTML/CSS/JS   | Frontend static site technology     |

---

## ⚙️ Installation

### 📦 Backend Setup

1. **Clone this repository**:
   ```bash
   git clone https://github.com/Siuli-Sharon-Sabnam/End-to-End-NLP-Chatbot.git
   cd End-to-End-NLP-Chatbot
   ```

2. **Install dependencies**:
   ```bash
   pip install -r backend/requirements.txt
   ```

   _Or individually_:
   ```bash
   pip install mysql-connector
   pip install "fastapi[all]"
   ```

3. **Start FastAPI server**:
   ```bash
   cd backend
   uvicorn main:app --reload
   ```

---

## 🛠 Database Setup

1. Open **MySQL Workbench**.
2. Create a new schema or use an existing one.
3. Import the `.sql` file from the `db/` folder.

---

## 🌐 Ngrok for HTTPS (Required by Dialogflow)

1. Download ngrok from [https://ngrok.com/download](https://ngrok.com/download)
2. Extract and run:
   ```bash
   ngrok http 8000
   ```
3. Copy the HTTPS URL generated and paste it into Dialogflow's webhook settings.

> ⚠️ Note: ngrok sessions can timeout; restart and update the URL if needed.

---

## 🧪 Dialogflow Setup

- Import `dialogflow_assets/` into Dialogflow agent.
- Configure the webhook URL to point to your ngrok HTTPS URL.
- Enable fulfillment for required intents.


