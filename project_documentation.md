# Local-First AI Assistant (TinyLlama & Flask)

A sleek, local-first, open-source full-stack AI web application featuring a high-tech sci-fi cobalt blue interface, live system resource monitoring, document parsing capabilities, and complete accessibility support. Built with a Flask backend and powered locally by Ollama (`tinyllama`).

---

## 🌟 Key Features

- **Local-First & Private:** Runs entirely on your local machine using Ollama and TinyLlama. Your data never leaves your computer.
- **Sci-Fi Cobalt Blue UI:** Immersive dark aesthetic featuring a holographic circular pulse avatar video element and high-contrast neon cyan interactive states.
- **Real-Time System Monitoring:** Live-updating performance bars tracking CPU, RAM, and SSD metrics via backend system polling.
- **Document Context Analysis:** Upload PDFs or text files to instantly parse content directly into RAM cache for context-aware Q&A.
- **Accessibility & Keyboard Navigation:** Fully optimized for low-vision and keyboard-only navigation with `:focus-visible` styling, logical tab flows, and clean ARIA labeling.
- **Speech Synthesis Integration:** Built-in text-to-speech reading controls for AI responses.

---

## 📁 Project Architecture

```text
project-future/
│
├── ai.py              # Core AI engine, document parser, and system stats monitor
├── app.py             # Flask background server with REST endpoints
├── index.html         # Main frontend UI structure
├── script.js          # Frontend event handlers, chat rendering, & stats polling
├── style.css          # Sci-fi cobalt blue styling and focus management
├── setup.bat          # Automated installation and dependency script
├── start_hidden.vbs   # Background service wrapper script
├── graphics/          # Visual assets (e.g., VEO.mp4)
├── Sounds/            # Audio assets (e.g., thinking.wav)
└── uploads/           # Temporary storage for parsed document nodes
```

---

## 🚀 Installation & Setup

### Automated Installation (Recommended for Windows)
1. Ensure your project folder is placed on a local drive path (e.g., `C:\project-future`).
2. Double-click **`setup.bat`**. 
3. The script will automatically check for Python, install required dependencies (`flask`, `flask-cors`, `pypdf`, `ollama`, `psutil`), download the `tinyllama` model, create a desktop shortcut, and launch your application in your default browser.

### Manual Installation
If you prefer manual setup:
```bash
# 1. Install required Python packages
pip install flask flask-cors pypdf ollama psutil

# 2. Ensure Ollama is installed and run the TinyLlama model
ollama pull tinyllama

# 3. Start the Flask backend server
python app.py
```
Open `index.html` in your web browser to interact with the application.

---

## ⌨️ Accessibility Shortcuts

| Command | Action |
| :--- | :--- |
| **`Enter`** | Send message |
| **`Alt + I`** | Focus input text area |
| **`Alt + F`** | Attach document file |
| **`Alt + O`** | Start new chat / clear memory |
| **`Alt + C`** | Copy last AI response |
| **`Alt + R`** | Read aloud (TTS) last AI response |

---

## 🛠️ Tech Stack

- **Backend:** Python, Flask, Ollama (`tinyllama`), `psutil`, `pypdf`
- **Frontend:** HTML5, CSS3 (Custom Sci-Fi Cobalt Theme), Vanilla JavaScript
- **Accessibility:** ARIA live regions, high-contrast cyan focus rings, keyboard tab-loop optimization