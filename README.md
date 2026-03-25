# whaatai-web


# ⚡ WhaatAI 

WhaatAI is a modern, responsive, and blazing-fast web interface for Large Language Models (LLMs). Designed with a focus on privacy and user experience, it allows users to interact with AI for general chat, code generation, and image creation. 

Currently configured for local execution via Ollama, WhaatAI ensures 100% data privacy by running inference directly on the host machine, with an architecture designed to easily scale to cloud-based APIs.

## 👨‍💻 Developer
**Adarsh Kumar Tiwari** *B.Tech Computer Science Engineering (1st Year)* *Centurion University of Technology and Management, Bhubaneswar*

## ✨ Features
* **💬 General Chat:** Fluid, responsive chat interface with markdown parsing and code syntax highlighting.
* **👨‍💻 Code Studio:** Dedicated coding workspace with language selection, one-click copy, and file download functionality.
* **🖼️ Image Generation:** UI ready for integration with Stable Diffusion (Automatic1111) or cloud image models.
* **⚙️ Dynamic Settings:** Adjustable AI parameters including temperature, max tokens, and system prompts.
* **📱 Responsive UI:** Clean, dark-mode-first design built with CSS variables and modern flexbox layouts.

## 🛠️ Tech Stack
* **Frontend:** HTML5, CSS3, Vanilla JavaScript (ES6+)
* **Backend Engine:** Ollama (Local AI Server)
* **Libraries:** Highlight.js (for code formatting)
* **Fonts:** Space Mono, Syne (via Google Fonts)

## 🚀 How to Run Locally

1. **Install Ollama:** Download and install [Ollama](https://ollama.com/).
2. **Pull a Model:** Open your terminal/command prompt and run:
   ```bash
   ollama pull llama3.2:3b
3. Configure CORS: Set the environment variable to allow local browser connections:

   Windows: Add a system environment variable OLLAMA_ORIGINS with the value *.

   Mac/Linux: Run OLLAMA_ORIGINS="*" ollama serve in the terminal.

4. Launch: Open index.html in any modern web browser.

🔮 Future Scope
Cloud API Integration: Migrating from local Ollama to serverless Cloud APIs (e.g., Groq, Gemini) for global, public deployment.

Authentication: Implementing secure user login and chat history saving via cloud databases.

Backend Development: Building a dedicated Node.js or Java backend to securely manage API keys and user data.
