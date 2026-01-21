# 🎙️ Voice AI Agent (Initial Release)

A browser-based voice-first AI agent that listens, thinks, and speaks back in real time.  
This initial release focuses on **core architecture correctness**, clean data flow, and a stable voice loop.

---

## ✨ Features

- 🎤 Voice input using browser Speech Recognition
- 🧠 AI-powered responses via LLM (Gemini)
- 🔊 Natural voice output using ElevenLabs
- 💬 Live chat transcript (User + AI)
- 🔁 Automatic loop: Listen → Think → Speak
- 📊 Agent status dashboard (state, turns)

---

## 🗒️ **Design highlights:**
- AI text is returned via HTTP **response headers** (`ai_text`)
- Audio is returned as **binary** (`audio/mpeg`) in response body
- Browser never parses audio as text

---

## 🧱 Tech Stack

### Frontend
- HTML / CSS / Vanilla JavaScript
- Web Speech API (SpeechRecognition)
- Native Audio API

### Backend / Orchestration
- n8n (Webhook-based workflow)

### AI Services
- Gemini (LLM)
- ElevenLabs (Text-to-Speech)

---

## 🚀 Getting Started

1. Run n8n and activate the workflow  
2. Configure Gemini & ElevenLabs API keys in n8n  
3. Ensure webhook URL matches `index.html`  
4. Open `index.html` in the browser  
5. Click 🧠 and start speaking

---

## ⚠️ Known Limitations (Initial Release)

- Browser-dependent speech recognition
- No long-term memory
- No streaming responses
- Single agent personality
- Audio requires user interaction to unlock (browser policy)

---



## 📜 License

MIT License

---

Built by **Kushagra**  
