# 🎙️ VOCA — Browser-Based AI Voice Assistant

VOCA is a lightweight AI voice assistant that runs directly in the browser.  
Users can interact with the assistant using **voice or text**, and responses are returned in both **text and synthesized speech**.

The project demonstrates how browser-native speech APIs can be combined with a large language model to create a **real-time conversational interface** without relying on expensive speech-processing services.

---

## 🚀 Features

- 🎤 **Voice Input** — Speak directly using the browser microphone  
- 🔊 **Voice Output** — AI responses are read aloud automatically  
- 🧠 **Conversation Memory** — Maintains context during the session  
- 🎭 **Multiple Voices** — Choose from available system voices  
- 🌙 **Dark / Light Mode** — Switch themes anytime  
- 🔁 **Replay Responses** — Listen to previous replies again  
- ↺ **Reset Conversation** — Clear chat history instantly  

---

## 🧠 Tech Stack

| Layer | Technology |
|------|------------|
| Backend | Python + Flask |
| AI Model | Llama 3 via Groq API |
| Speech Recognition | Web Speech API |
| Text-to-Speech | SpeechSynthesis API |
| Frontend | HTML · CSS · JavaScript |

---

## ⚙️ Architecture

```
User (Voice/Text)
      │
      ▼
Browser Speech Recognition
      │
      ▼
Frontend (JavaScript)
      │
      ▼
Flask Backend
      │
      ▼
Groq API (Llama 3)
      │
      ▼
AI Response
      │
      ▼
SpeechSynthesis API
      │
      ▼
Voice Output
```

---

## 📁 Project Structure

```
voca-assistant/
│
├── server.py            # Flask server & API routes
├── worker.py            # Groq AI integration + memory handling
├── requirements.txt     # Python dependencies
├── .env.example         # Environment variables template
├── .gitignore
│
├── static/
│   ├── script.js        # Frontend logic
│   └── style.css        # UI styling
│
└── templates/
    └── index.html       # Main application page
```

---

## 🛠️ Installation

### 1. Clone the repository

```bash
git clone https://github.com/YOUR_USERNAME/voca-assistant.git
cd voca-assistant
```

### 2. Install dependencies

```bash
pip install -r requirements.txt
```

### 3. Create environment variables

Create a `.env` file in the project root:

```
GROQ_API_KEY=your_api_key_here
```

You can get a free API key from:

https://console.groq.com

---

### 4. Run the server

```bash
python server.py
```

Open the application in your browser:

```
http://localhost:8000
```

---

## ⚠️ Notes

- Microphone input works best in **Chrome or Edge**
- Conversation history resets when the page refreshes
- Groq free tier has request limits

---

## 📄 License

MIT License
