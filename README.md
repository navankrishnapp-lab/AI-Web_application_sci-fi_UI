AI Web Application Sci-Fi UI
A local first, privacy centered AI assistant featuring an immersive cyber blue interface, live hardware performance monitoring, document parsing capabilities, and complete screen reader accessibility. Built with a lightweight Python Flask backend and powered locally on device by Ollama running TinyLlama.
Overview
Most AI web tools require cloud communication, store user data on remote servers, or feature busy interfaces that fail keyboard navigation and accessibility standards.
This project demonstrates a sci fi cyber aesthetic combined with complete data privacy and accessibility. Everything processes directly on your local machine using a compact TinyLlama model through Ollama, meaning your conversations and uploaded documents never touch an external network.
Key Features
Local Privacy. Runs offline on your machine using Ollama and TinyLlama. No external API keys or cloud relays required.
Real Time Hardware Telemetry. Embedded status monitors track live CPU, RAM, and primary drive usage percentages through background system polling.
Document Ingestion. Upload PDF or text files to load document contents into fast local memory for context aware questions and summaries.
Accessible Audio Feedback. Built in Web Speech API synthesis reads AI responses aloud, with automatic removal of distracting markdown symbols, asterisks, and emojis before speech begins.
Keyboard First Navigation. Complete shortcut support, clear high contrast focus indicators, and ARIA attributes for seamless navigation without requiring a mouse.
Memory Control. Dedicated memory clearing routines allow full cache clearing between tasks with a single shortcut.
User Interface and Aesthetic
Split Pane Layout. The left side features a looping circular pulse avatar animation, while the right side houses live hardware telemetry and conversational history.
Pure Black High Contrast Mode. Deep black backgrounds paired with high tech cobalt and neon cyan accents to prevent visual fatigue while keeping contrast sharp.
Responsive Chat Stream. Dynamic bubbles for user queries and AI outputs with integrated one click copy and text to speech actions.
Tech Stack
Frontend. HTML5, CSS3 with a pure black and cobalt theme and safe viewports, and Vanilla JavaScript ES6 plus.
Backend. Python 3, Flask, and Flask CORS.
Local Intelligence. Ollama with the TinyLlama model.
Document Extraction. PyPDF.
System Monitoring. Psutil.
Repository Structure
index.html. Main semantic interface, status indicators, and input panel.
style.css. Cobalt blue cyber styling, accessible focus rings, and layout rules.
script.js. Telemetry polling, keyboard shortcuts, speech engine, and API communication.
app.py. Flask REST server providing endpoints for chat, uploads, and telemetry.
ai.py. Core TinyLlama bridge, PDF cache extractor, and hardware statistics engine.
setup.bat. Automated Windows setup script for installing dependencies and models.
start_hidden.vbs. VBScript wrapper to run the Flask backend silently in the background.
Keyboard Shortcuts
Enter. Send message when focused on the input box.
Alt and I. Focus the text input box.
Alt and F. Attach a document file.
Alt and O. Start a new chat and wipe the memory cache.
Alt and C. Copy the most recent AI response to the clipboard.
Alt and R. Read the most recent AI response aloud using speech synthesis.
Tab and Shift plus Tab. Cycle between input and send actions.
Setup and Installation
Option 1. Automated Setup on Windows.
Step 1. Clone or download this repository onto your machine.
Step 2. Run setup.bat by double clicking it.
Step 3. The script will automatically verify Python, install required packages including Flask, Flask CORS, PyPDF, Ollama, and Psutil, download the TinyLlama model through Ollama, create a desktop shortcut, and launch the application.
Option 2. Manual Installation on All Platforms.
Step 1. Clone the repository.
git clone https://github.com/navankrishnapp-lab/AI-Web_application_sci-fi_UI.git
Step 2. Navigate into the project folder.
cd AI-Web_application_sci-fi_UI
Step 3. Install Python dependencies.
pip install flask flask-cors pypdf ollama psutil
Step 4. Install and start Ollama.
Ensure Ollama is installed on your operating system from https://ollama.com. Then download the TinyLlama model.
ollama pull tinyllama
Step 5. Start the Flask application backend.
python app.py
Step 6. Open the interface.
Open index.html in your preferred web browser.
API Endpoints
POST /chat. Accepts a JSON prompt payload and returns generated responses from TinyLlama.
POST /upload. Ingests PDF or text files into temporary server memory for contextual questioning.
GET /system-stats. Returns real time CPU, RAM, and disk utilization percentages.
POST /reset. Flushes cached document context and resets the active model state.
Author and Acknowledgments
Developed by Navan Krishna.
Design Focus. Universal accessibility, digital privacy, and futuristic user interfaces.
License
This project is open source under the MIT License. You are free to modify, expand, and distribute it.
