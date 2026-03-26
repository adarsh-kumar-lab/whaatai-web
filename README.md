# ⚡ WhaatAI — Free AI Chat Interface

<div align="center">

![WhaatAI Banner](https://img.shields.io/badge/WhaatAI-RED%20EDITION-ff1a1a?style=for-the-badge&logo=lightning&logoColor=white)
![License](https://img.shields.io/badge/License-MIT-red?style=for-the-badge)
![HTML](https://img.shields.io/badge/HTML5-Pure%20Vanilla-ff1a1a?style=for-the-badge&logo=html5&logoColor=white)
![CSS](https://img.shields.io/badge/CSS3-No%20Framework-cc0000?style=for-the-badge&logo=css3&logoColor=white)
![JS](https://img.shields.io/badge/JavaScript-ES2022-ff4444?style=for-the-badge&logo=javascript&logoColor=white)

**A fully-featured AI chat interface — 100% free, zero dependencies, runs in any browser.**

[🚀 Live Demo](#) · [📖 Docs](#setup) · [🐛 Issues](../../issues) · [⭐ Star this repo](#)

</div>

---

## ✨ Features

| Feature | Description |
|---|---|
| 💬 **AI Chat** | Real-time streaming chat with full markdown rendering |
| 👾 **Code Studio** | AI-powered code generation in 9 languages |
| 🗂️ **Chat History** | Persistent conversations saved in localStorage |
| ⚙️ **Configurable** | Custom system prompt, temperature, max tokens |
| 🎨 **Red Edition UI** | Custom design system with animated background grid |
| ⚡ **Zero Dependencies** | Pure HTML, CSS, JS — no npm, no build step |
| 🆓 **100% Free** | Uses Groq's free API tier — no credit card needed |

---

## 🖼️ Screenshots

> _Add your screenshots here after cloning_

---

## 🚀 Setup

### 1. Clone the repository
```bash
git clone https://github.com/YOUR_USERNAME/WhaatAI.git
cd WhaatAI
```

### 2. Get a free Groq API key
1. Go to [console.groq.com](https://console.groq.com)
2. Sign up for free
3. Create an API key (starts with `gsk_...`)
4. No credit card required ✅

### 3. Open in browser
```bash
# Just double-click index.html
# OR serve locally:
python -m http.server 8000
# Then open http://localhost:8000
```

### 4. Add your API key
- Open WhaatAI in your browser
- Click **⚙️ Config** tab
- Paste your Groq API key
- Click **Save Configuration**

That's it! 🎉

---

## 🧠 Supported Models

| Model | Speed | Context | Best For |
|---|---|---|---|
| `llama-3.1-8b-instant` | ⚡ Fastest | 128K | Everyday chat |
| `llama-3.3-70b-versatile` | 🧠 Smart | 128K | Complex reasoning |
| `mixtral-8x7b-32768` | 📚 Long | 32K | Long documents |

---

## 🗂️ Project Structure

```
WhaatAI/
│
├── index.html          # Everything — single file app
│
└── README.md           # This file
```

> Single-file architecture — the entire app lives in `index.html`. No build tools, no node_modules, no complexity.

---

## 🛠️ Tech Stack

- **HTML5** — semantic structure
- **CSS3** — custom design system with CSS variables, animations, grid
- **JavaScript (ES2022)** — async/await, streaming fetch, localStorage
- **Groq API** — ultra-fast LLM inference (free tier)
- **Highlight.js** — syntax highlighting for code blocks

---

## 🎨 Design System

The Red Edition uses a carefully crafted design system:

```css
--r1: #ff1a1a   /* Primary red   */
--r2: #cc0000   /* Deep crimson  */
--r3: #ff4444   /* Soft red      */
--r4: #ff6666   /* Highlight     */
```

- Animated background grid
- Glowing red accents with CSS `box-shadow`
- `Outfit` display font + `JetBrains Mono` for code
- Glassmorphism input area with `backdrop-filter`
- Smooth CSS transitions on every interactive element

---

## 📝 License

MIT License — free to use, modify, and distribute.

---

## 👤 Author

**Your Name**
- GitHub: @adarsh-kumar-lab , https://github.com/adarsh-kumar-lab
- LinkedIn: www.linkedin.com/in/adarsh-kumar-tiwari-376a0b386

---

<div align="center">
  <strong>If you found this useful, please ⭐ star the repo!</strong>
</div>
