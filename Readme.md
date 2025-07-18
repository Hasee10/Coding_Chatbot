# AIVA Prompt Improver: Local-First AI Prompt Enhancement Dashboard

![Dashboard Screenshot](1.png)

---

## 🚀 Introduction

**AIVA Prompt Improver** is a privacy-first, local AI assistant that helps you rewrite and enhance your prompts for use with AI models. It runs entirely on your machine—no cloud, no external APIs—offering chat, prompt improvement, and a beautiful, modern UI. Whether you're a prompt engineer, researcher, or everyday user, AIVA helps you craft better prompts for any AI system.

---

## 🏗️ Architecture & Tech Stack

- **Frontend:** React (Vite), Tailwind CSS
- **Backend:** Node.js (Express)
- **LLM Serving:** Ollama (TinyLlama, Phi-3)
- **Storage:** Browser localStorage (sessions)
- **No Cloud:** All processing is local

---

## 📁 Folder Structure

```
New_Chatbot/
├── 1.png                # Dashboard screenshot
├── backend/             # Node.js server (API)
│   ├── index.js         # Express server
│   ├── package.json     # Backend dependencies
├── frontend/            # React app (UI)
│   ├── index.html       # App entry
│   ├── package.json     # Frontend dependencies
│   ├── tailwind.config.js # Custom theme
│   ├── postcss.config.js  # Tailwind/PostCSS setup
│   └── src/
│       ├── App.jsx      # Main app logic
│       ├── index.jsx    # React entry
│       ├── index.css    # Global styles
│       └── components/  # UI components
├── main_ideas.txt       # Project vision & notes
└── README.md            # This file
```

---

## ✨ Features

### Frontend (React + Tailwind)
- **Modern UI:** Sidebar, chat thread, model switcher, input bar, context panel
- **Chat History:** Persistent sessions, easy switching, delete & create new chats
- **Model Switching:** Instantly toggle between TinyLlama and Phi-3
- **Prompt Improvement:** Paste or type your prompt, and the bot will rewrite it for clarity, detail, and effectiveness
- **Prompt Templates:** Use the + button to quickly insert common prompt types (summarize, translate, rewrite, etc.)
- **Search:** Search through your chat history with the search button
- **Pro Mode:** Toggle advanced prompt improvement (uses best model or advanced instructions)
- **Copy to Clipboard:** Copy any message (user or AI) with one click
- **Responsive Design:** Works on desktop and tablets

### Backend (Node.js/Express)
- **/chat:** Forwards user prompt to Ollama with special instructions to improve the prompt, returns the improved prompt
- **Pro Mode:** Uses advanced model or instructions for better results
- **No Cloud:** All processing is local, no external API calls

---

## 🖼️ Dashboard Preview

![Dashboard UI](1.png)

---

## 🧩 How It Works

1. **Start the backend server** (Node.js/Express)
2. **Start Ollama** and run a local LLM (Phi-3 or TinyLlama)
3. **Start the frontend** (React/Vite)
4. **Open the dashboard in your browser**
5. **Paste or type your prompt** and get an improved version instantly
6. **Use the + button** for quick prompt templates, or the search button to find previous messages
7. **Toggle Pro mode** for advanced prompt enhancement

---

## 🛠️ Setup Instructions

### 1. Prerequisites
- **Node.js** (v16+ recommended)
- **npm** (comes with Node.js)
- **Ollama** (for local LLMs: [Ollama Download](<insert-link-here>))

### 2. Clone the Repository
```bash
git clone <your-repo-url>
cd New_Chatbot
```

### 3. Backend Setup
```bash
cd backend
npm install
node index.js
# Backend runs on http://localhost:3001
```

### 4. Frontend Setup
```bash
cd ../frontend
npm install
npm run dev
# Frontend runs on http://localhost:5173 (default Vite port)
```

### 5. Ollama Setup
- Download and install Ollama from [Ollama Download](<insert-link-here>)
- Pull the required models:
```bash
ollama pull tinyllama
ollama pull phi3
ollama run phi3
```
- Ollama API runs on http://localhost:11434

---

## 🧑‍💻 Usage Guide

1. **Start Backend:** `node backend/index.js`
2. **Start Ollama:** `ollama run phi3` (or tinyllama)
3. **Start Frontend:** `npm run dev` in `frontend/`
4. **Open in Browser:** [http://localhost:5173](http://localhost:5173)
5. **Paste your prompt and get an improved version instantly!**
6. **Use the + button for templates, Search for history, and Pro for advanced mode**

---

## 🖌️ Design System
- **Colors:** Deep green, olive, cream, peach, mint, pastel green
- **Fonts:** Inter, Manrope (Google Fonts)
- **Cards:** `rounded-2xl`, `shadow-lg`, `p-4`
- **Buttons:** `rounded-2xl`, `hover:bg-green-700`, `transition`
- **Typography:** `font-sans`, `text-lg`, `font-medium`
- **Responsiveness:** `md:flex`, `w-full`, `max-w-4xl`, etc.

---

## 🔒 Security & Privacy
- All chat and data processing is done **locally**
- No cloud APIs, no data leaves your machine
- No tracking, analytics, or telemetry
- Perfect for privacy-focused users and enterprise environments

---

## 🧩 Customization
- **Add new models:** Edit `MODELS` in `App.jsx`
- **Change theme:** Edit `tailwind.config.js`
- **Add endpoints:** Extend `backend/index.js`
- **Add prompt templates:** Edit the `PROMPT_TEMPLATES` array in `InputBar.jsx`

---

## 🐞 Troubleshooting & FAQ

- **Ollama not running?**
  - Make sure `ollama run <model>` is active and listening on port 11434
- **Frontend/Backend connection issues?**
  - Check CORS settings and port numbers
- **Changed folder location?**
  - Update any hardcoded paths if you moved the project (especially for LLM models)
- **Model not found?**
  - Make sure you have pulled the required models with `ollama pull <model>`

---

## 🤝 Contributing

We welcome contributions! To get started:
1. Fork this repo and clone it locally
2. Create a new branch for your feature or bugfix
3. Make your changes and commit them with clear messages
4. Push to your fork and open a Pull Request

- [Contribution Guide](<insert-link-here>)
- [Open Issues](<insert-link-here>)
- [Discussions](<insert-link-here>)

---

## 🗺️ Roadmap
- [ ] Add more prompt templates and customization options
- [ ] Add user authentication (optional/local)
- [ ] Export/import chat history
- [ ] Add more LLM models and model settings
- [ ] Mobile-first UI improvements
- [ ] <Add your suggestions!>

---

## 🙏 Credits & Acknowledgments
- **Ollama** for local LLM serving ([Ollama Website](<insert-link-here>))
- **React** & **Tailwind CSS** for the beautiful UI
- **All contributors and users!**

---

## 📄 Project Vision

See `main_ideas.txt` for the full vision, roadmap, and design philosophy behind AIVA Prompt Improver.

---

## 📚 Links & Resources
- **Live Demo:** <insert-link-here>
- **Documentation:** <insert-link-here>
- **Report Issues:** <insert-link-here>
- **Community/Chat:** <insert-link-here>
- **License:** <insert-link-here>

---

**Enjoy your private, local-first AI prompt improvement dashboard!** 
