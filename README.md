# ⚡ WhaatAI — Free AI Chat Interface

<div align="center">

![WhaatAI](https://img.shields.io/badge/WhaatAI-RED%20EDITION-ff1a1a?style=for-the-badge&logoColor=white)
![PWA](https://img.shields.io/badge/PWA-Installable-cc0000?style=for-the-badge&logo=pwa&logoColor=white)
![License](https://img.shields.io/badge/License-MIT-ff4444?style=for-the-badge)
![HTML](https://img.shields.io/badge/HTML5-Pure%20Vanilla-ff1a1a?style=for-the-badge&logo=html5&logoColor=white)
![CSS](https://img.shields.io/badge/CSS3-No%20Framework-cc0000?style=for-the-badge&logo=css3&logoColor=white)
![JS](https://img.shields.io/badge/JavaScript-ES2022-ff4444?style=for-the-badge&logo=javascript&logoColor=white)

**A fully-featured, free AI chat interface — installable on laptop and phone as a PWA.**  
**No frameworks. No npm. No subscriptions. Just open and use.**

[🚀 Live Demo](#) · [🐛 Issues](../../issues) · [⭐ Star this repo](#)

</div>

---

## 📖 Table of Contents

- [What is WhaatAI?](#what-is-whaatai)
- [Features](#features)
- [Project Structure](#project-structure)
- [Quick Start](#quick-start)
- [Install as an App](#install-as-an-app)
- [Tech Stack](#tech-stack)
- [Design System](#design-system)
- [Supported Models](#supported-models)
- [Full Build Journey](#full-build-journey)
- [Bugs Found & Fixed](#bugs-found--fixed)
- [Troubleshooting](#troubleshooting)
- [License](#license)

---

## What is WhaatAI?

WhaatAI is a personal AI chat interface I built from scratch — a single HTML file that works like a full app. It connects to the **Groq API** (completely free, ultra-fast) and gives you a beautiful, dark red interface similar to Claude or ChatGPT, but:

- ✅ 100% free forever
- ✅ No account needed beyond Groq (also free)
- ✅ Runs on your laptop, phone, or anywhere with a browser
- ✅ Installable as a real app (PWA) — no app store needed
- ✅ Your conversations stay on your device
- ✅ Zero dependencies, zero build tools, zero complexity

---

## Features

| Feature | Description |
|---|---|
| 💬 **Streaming Chat** | Real-time AI responses, word by word as they generate |
| 👾 **Code Studio** | AI code generation in 9 languages with syntax highlighting |
| 🗂️ **Chat History** | Saves your last 25 conversations in the browser |
| 🎨 **Red Edition UI** | Custom dark design system with animated grid background |
| 📱 **PWA / Installable** | Install on phone home screen or laptop like a native app |
| 📲 **Mobile Bottom Nav** | Touch-friendly navigation bar on phones |
| 🔑 **Persistent API Key** | Your key saves locally — enter once, works forever |
| ⚙️ **Configurable** | Temperature, max tokens, system prompt all adjustable |
| 📋 **Copy Buttons** | One-click copy on every AI message and code block |
| 🆓 **100% Free** | Groq API free tier — no credit card, no limits |

---

## Project Structure

```
WhaatAI/
│
├── index.html       ← Entire app: HTML + CSS + JavaScript in one file
├── manifest.json    ← PWA config: name, icon, colors, display mode
├── sw.js            ← Service Worker: enables install + offline shell
├── icon-192.svg     ← App icon (small) — home screen / taskbar
├── icon-512.svg     ← App icon (large) — splash screen
└── README.md        ← This file
```

> **Why single file?** No build step, no node_modules, no webpack. Anyone can open it, read it, and understand it. Perfect for learning and for a portfolio.

---

## Quick Start

### 1. Clone or download
```bash
git clone https://github.com/YOUR_USERNAME/WhaatAI.git
cd WhaatAI
```

### 2. Get a free Groq API key
1. Go to **[console.groq.com](https://console.groq.com)**
2. Sign up — completely free, no credit card
3. Click **API Keys** → **Create API Key**
4. Copy the key — it starts with `gsk_...`

### 3. Open the app
```bash
# Option A — just double-click index.html in your file explorer
# Option B — serve locally for PWA features:
python -m http.server 8000
# then open http://localhost:8000 in Chrome
```

### 4. Enter your API key
1. Click **⚙️ Config** tab (top right on desktop, bottom right on mobile)
2. Paste your `gsk_...` key in the **Groq API Key** field
3. Click **Save Key** or **Save Configuration**
4. Done — the key is saved permanently in your browser ✅

---

## Install as an App

### 💻 Laptop (Windows / Mac / Linux)
> Works in Chrome or Edge only

1. Push all 5 files to GitHub
2. Enable **GitHub Pages**: Settings → Pages → Deploy from `main` branch
3. Open your live GitHub Pages link in **Chrome or Edge**
4. Look for the **install icon** `⊕` in the address bar
5. Click it → **Install** → WhaatAI appears in your Start Menu / Applications ✅

### 📱 Android Phone
1. Open your GitHub Pages link in **Chrome**
2. After 3 seconds, a red install banner appears automatically
3. Tap **Install** → icon added to home screen
4. Opens fullscreen like a real app, no browser bar ✅

### 🍎 iPhone / iPad
1. Open your GitHub Pages link in **Safari** (must be Safari, not Chrome)
2. Tap the **Share button** (box with upward arrow at bottom)
3. Scroll down → tap **"Add to Home Screen"**
4. Tap **Add** in the top right
5. WhaatAI appears on your home screen ✅

---

## Tech Stack

| Technology | What it does |
|---|---|
| **HTML5** | Structure and layout |
| **CSS3** | Full custom design system — variables, animations, grid, glassmorphism |
| **JavaScript ES2022** | Async/await, streaming fetch, localStorage, service worker |
| **Groq API** | Free, ultra-fast AI inference (OpenAI-compatible format) |
| **Highlight.js** | Syntax highlighting for code blocks (loaded from CDN) |
| **Google Fonts** | Outfit (UI font) + JetBrains Mono (code font) |
| **PWA / Service Worker** | Makes the app installable and gives it an offline shell |

---

## Design System

The Red Edition uses a custom CSS variable design system:

```css
/* Color Palette */
--bg:    #080608   /* Pure black background     */
--panel: #110d10   /* Sidebar / topbar surface  */
--card:  #180f16   /* Card background           */
--r1:    #ff1a1a   /* Primary red — main accent */
--r2:    #cc0000   /* Deep crimson              */
--r3:    #ff4444   /* Soft red — text accents   */
--r4:    #ff6666   /* Highlight red             */
```

**Visual effects used:**
- Animated background grid (CSS `background-image` + `@keyframes`)
- Glowing logo with `box-shadow` animation
- Red gradient text using `-webkit-background-clip: text`
- Glassmorphism input with `backdrop-filter: blur()`
- Red scanline under topbar using `::after` pseudo-element
- Smooth transitions on every interactive element

---

## Supported Models

| Model | Speed | Best For |
|---|---|---|
| `llama-3.1-8b-instant` | ⚡ Fastest | Everyday chat, quick answers |
| `llama-3.3-70b-versatile` | 🧠 Smartest | Complex reasoning, writing |
| `mixtral-8x7b-32768` | 📚 Long context | Long documents, research |

All models are free on Groq's free tier with generous rate limits.

---

## Full Build Journey

This section documents exactly how WhaatAI was built — every version, every decision, every improvement.

---

### Version 1 — The Beginning

**What was built:**
The first version was a complete AI chat interface with everything working out of the box:

- Full chat UI with streaming responses
- Sidebar with chat history
- Model selector (Ollama local models)
- Code generation tab
- Image generation tab (Stable Diffusion)
- Voice input
- File attachment support
- Settings panel
- Dark theme with purple accents

**Tech decisions:**
- Used **Ollama** for local AI (runs models on your own computer)
- Pure HTML/CSS/JS — no frameworks
- localStorage for saving conversations and settings
- Streaming fetch for real-time responses

**Hardware context:**
Built for an HP Laptop 15s with:
- Intel Core i3-1005G1 @ 1.20GHz
- 12GB RAM (11.8GB usable)
- Intel UHD Graphics (128MB)
- Windows 11 Home

This is why local models like `llama3.2:3b` were recommended — small enough to run on this hardware.

---

### Version 2 — UI Redesign (Purple Theme)

**Problem:** The original design was too basic — generic dark theme, not portfolio-worthy.

**What changed:**
- Switched from purple/dark blue to a deeper navy palette
- Added `Inter` font (clean, modern)
- `JetBrains Mono` for code blocks
- Rounded corners everywhere (14-22px radius)
- Gradient send button with glow
- Better code block headers with language labels
- Hover-to-reveal copy button on messages
- Smooth animations on all interactions

---

### Version 3 — RED EDITION (Current)

**Reason:** Wanted something bold, memorable, and unique for a GitHub portfolio project.

**Design direction:** Deep crimson luxury meets cyberpunk precision.

**What was redesigned:**
- Complete color system replaced with 6 shades of red
- Animated background grid that slowly drifts
- Glowing red logo that pulses
- Red gradient text on the welcome screen title
- Red left-border accent on AI messages
- Red scanline under the topbar (using CSS `::after`)
- Vertical red accent stripe on sidebar
- `Outfit` font (bold, modern, distinctive)
- Feature tags on welcome screen
- 6 quick-start prompt buttons
- Card system with red top accent line
- Red dot status indicators with glow animation

**Switched from Ollama to Groq API:**
- Ollama requires installing software locally — harder to share
- Groq API is free, requires no installation, works from any browser
- 10x faster responses than running locally on i3 hardware
- Better for a portfolio project others can actually use

---

### Version 4 — PWA (Installable App)

**Goal:** Make WhaatAI installable on laptop and phone like a real app.

**What was added:**

**`manifest.json`** — tells the browser this is an installable app:
```json
{
  "name": "WhaatAI",
  "display": "standalone",
  "theme_color": "#ff1a1a",
  "background_color": "#080608"
}
```

**`sw.js`** (Service Worker) — enables installation and offline shell:
```js
// Caches the app shell so it loads even without internet
// API calls always go to network (never cached)
```

**Mobile bottom navigation bar:**
- Hidden on desktop, shows on screens under 700px
- 4 buttons: Chat, New, Code, Config
- Red active indicator
- Handles iOS safe area (notch) with `env(safe-area-inset-bottom)`

**Full responsive CSS:**
- Mobile: sidebar hidden, bottom nav shown, larger tap targets
- Tablet: narrower sidebar (220px)
- Desktop: full sidebar (268px)

**Install banner:**
- Appears automatically after 3 seconds on first visit
- Dismissible (remembers your choice in localStorage)
- Uses native `beforeinstallprompt` browser event

---

## Bugs Found & Fixed

This section documents every problem that was found and exactly how it was fixed. If you hit the same issue, the solution is here.

---

### 🐛 Bug 1 — API Key Not Saving

**Symptom:**  
You enter your Groq API key in Settings, click Save, close the app, reopen it — the key is gone. You have to re-enter it every time.

**Root cause:**  
The Settings panel uses `display:none` to hide until the user clicks the Config tab. When the page first loads, `loadSettings()` tried to fill the API key input field with the saved value — but the browser couldn't find the element because the panel wasn't rendered yet.

```js
// ❌ BROKEN — runs on page load, but #api-key-input is in a hidden panel
function loadSettings() {
  const p = JSON.parse(localStorage.getItem('whaat_settings_v3'));
  if (p.apiKey) {
    apiKey = p.apiKey;
    document.getElementById('api-key-input').value = apiKey; // ← FAILS silently
  }
}
```

**Fix:**  
Split into two functions:
1. `loadSettings()` — only reads from localStorage into JS variables (no DOM touching)
2. `populateSettingsFields()` — fills the input fields, called only when the Settings tab is actually opened

```js
// ✅ FIXED — load into variable only
function loadSettings() {
  const s = localStorage.getItem('whaat_settings_v3');
  if (s) {
    const p = JSON.parse(s);
    settings = { ...settings, ...p };
    if (p.apiKey) { apiKey = p.apiKey; }  // ← just the variable, no DOM
    if (p.model)  { selectedModel = p.model; }
  }
}

// ✅ Called only when tab opens
function populateSettingsFields() {
  document.getElementById('api-key-input').value    = apiKey;
  document.getElementById('system-prompt').value    = settings.systemPrompt || '';
  document.getElementById('temp-range').value       = settings.temperature;
  document.getElementById('tokens-range').value     = settings.maxTokens;
}

// ✅ Trigger population when tab is switched
function switchTab(tab, btn) {
  // ...
  if (tab === 'settings') populateSettingsFields();
}
```

**Result:** API key now saves permanently. Enter once, works forever. ✅

---

### 🐛 Bug 2 — Settings Fields Invisible on Page Load

**Related to Bug 1.**

**Symptom:**  
Even after fixing the API key, fields like temperature slider and system prompt weren't showing their saved values when you opened Settings.

**Fix:**  
Same solution — `populateSettingsFields()` sets all fields at the moment the tab becomes visible, so they always show current values.

---

### 🐛 Bug 3 — Mobile Layout Broken

**Symptom:**  
On a phone, the sidebar overlapped the chat area, the tab buttons were too small to tap, and the input box was awkward to use.

**Fix:**  
Complete mobile-first responsive overhaul:

```css
@media(max-width:700px) {
  /* Hide desktop sidebar */
  #sidebar { display: none !important; }

  /* Show mobile bottom nav instead */
  #bottom-nav { display: block; }

  /* Hide desktop tab buttons */
  .t-right { display: none; }

  /* Bigger text in input to prevent iOS auto-zoom */
  #user-input { font-size: 16px; }

  /* Handle iPhone notch / home bar */
  #input-area {
    padding-bottom: calc(12px + env(safe-area-inset-bottom, 0px));
  }
}
```

---

### 🐛 Bug 4 — iOS Keyboard Pushes Layout Up

**Symptom:**  
On iPhone, when the keyboard opens, the input area gets pushed off screen.

**Fix:**  
Added `viewport-fit=cover` to the meta viewport tag and used CSS environment variables for safe area:

```html
<meta name="viewport" content="width=device-width, initial-scale=1.0, viewport-fit=cover"/>
```

```css
padding-bottom: env(safe-area-inset-bottom, 0px);
```

---

### 🐛 Bug 5 — PWA Install Banner Never Showed

**Symptom:**  
The install banner was coded but never appeared on Android Chrome.

**Root cause:**  
The `beforeinstallprompt` event only fires when:
1. The app is served over HTTPS (not `file://`)
2. A `manifest.json` is linked
3. A service worker is registered
4. The user hasn't already installed it

**Fix:**  
Deploy to GitHub Pages (which provides HTTPS automatically) and make sure all 5 files are in the repo root. The banner then appears correctly after 3 seconds.

---

### 🐛 Bug 6 — Code Copy Button Didn't Work

**Symptom:**  
Clicking "Copy" on a code block in the chat didn't copy anything.

**Root cause:**  
The `cpBlock()` function was looking for a sibling element using `.nextElementSibling` from the button, but after Highlight.js processed the code, the DOM structure changed.

**Fix:**  
Changed the selector to use `.closest()` to walk up to the parent container, then find the code element from there:

```js
// ❌ Broken — assumes specific sibling structure
function cpBlock(btn) {
  const code = btn.nextElementSibling.textContent;
}

// ✅ Fixed — walks up to container, finds code reliably
function cpBlock(btn) {
  const code = btn.closest('.code-block')?.querySelector('code')?.textContent || '';
  navigator.clipboard.writeText(code);
  btn.textContent = 'Copied!';
  setTimeout(() => btn.textContent = 'Copy', 1800);
}
```

---

### 🐛 Bug 7 — Service Worker Blocked API Calls

**Symptom:**  
After the service worker was registered, API calls to Groq stopped working because the SW tried to cache them.

**Fix:**  
Added network-only bypass for all external API domains:

```js
self.addEventListener('fetch', e => {
  // Never cache API calls — always go to network
  if (e.request.url.includes('groq.com') ||
      e.request.url.includes('googleapis.com') ||
      e.request.url.includes('cdnjs.cloudflare.com')) {
    return; // ← bypass service worker entirely
  }
  e.respondWith(
    caches.match(e.request).then(cached => cached || fetch(e.request))
  );
});
```

---

## Troubleshooting

### "Add your Groq API key in Settings" — even after I saved it

**Cause:** You may have opened `index.html` directly from the file system (`file://` URL).  
**Fix:** Serve it with a local server:
```bash
python -m http.server 8000
```
Or deploy to GitHub Pages and use that URL.

---

### The install button doesn't appear on laptop

**Cause:** PWAs only install from HTTPS. `file://` URLs don't work.  
**Fix:** Use GitHub Pages or any HTTPS host. On Chrome/Edge look for the ⊕ icon in the address bar.

---

### On iPhone, "Add to Home Screen" isn't working

**Cause:** You must use **Safari** on iOS. Chrome on iPhone doesn't support PWA installation.  
**Fix:** Open the GitHub Pages URL in Safari → Share button → Add to Home Screen.

---

### Streaming stops halfway through a response

**Cause:** Groq free tier has rate limits. You may have hit them.  
**Fix:** Wait 60 seconds and try again. Switch to a smaller model (`llama-3.1-8b-instant`) for faster responses that use less quota.

---

### The animated background grid is laggy on my phone

**Fix:** Add this to your CSS to force GPU acceleration:
```css
body::before {
  will-change: transform;
}
```

---

### Code isn't highlighting after AI response

**Cause:** Highlight.js loads from CDN — if you're offline, it won't load.  
**Fix:** Make sure you have internet when using the app. The code still shows, just without colors.

---

## License

MIT License — free to use, modify, distribute, and include in your own projects.

---

## 👤 Author

Built by me, with help from Claude AI for code generation and debugging.

**Replace with your info:**
- GitHub: [@YOUR_USERNAME](https://github.com/YOUR_USERNAME)
- LinkedIn: [your-linkedin](https://linkedin.com/in/YOUR_NAME)

---

<div align="center">

**If this helped you, please ⭐ star the repo — it means a lot!**

![Made with](https://img.shields.io/badge/Made%20with-HTML%20%2B%20CSS%20%2B%20JS-ff1a1a?style=flat-square)
![Powered by](https://img.shields.io/badge/Powered%20by-Groq%20API-cc0000?style=flat-square)
![Installable](https://img.shields.io/badge/PWA-Installable-ff4444?style=flat-square)

</div>






