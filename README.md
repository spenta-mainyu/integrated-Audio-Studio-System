# 🎛️ Audio Studio | Comprehensive Single-File Web Audio App

A feature-rich, **single-file** web application that runs entirely in your browser — combining **Text-to-Speech (TTS)**, **Speech-to-Text (STT)**, a **Gemini AI Chat Shortcut**, and a professional **Multi-Track Audio Editor**.

No installation, build tools, Node.js, or backend server required. Simply open the HTML file in any browser and start working immediately.

> 🔒 **100% Privacy-First:** Except for AI API calls (TTS/STT), all audio processing, editing, project state auto-saving, and sample storage are handled locally inside your browser using the Web Audio API and IndexedDB.

---

## ✨ Key Features & Capabilities

### 🗝️ API Key & Settings Management
- **Secure Local Storage:** API keys are stored safely in `localStorage`.
- **Live Key Validation:** Test API key validity with a single click.
- **Model Fetching:** Query and display available models live for your API key.
- **Latest Model Support:**
  - **TTS Models:** `gemini-3.8-flash-tts`, `gemini-3.8-flash-lite-tts`, `gemini-3.1-flash-tts-preview`, `gemini-2.5-pro-tts`, plus custom model entry.
  - **STT Models:** `gemini-3.5-transcribe` and `gemini-3.5-transcribe-live`.
- **Backup & Restore:** Export and import all settings and API keys as a `.json` file.

---

### 🔊 Text-to-Speech (TTS) Studio
- **Two Voice Modes:**
  - **Single Speaker:** Convert text to natural speech with custom voice selection.
  - **Two-Speaker Dialogue:** Define two speakers with custom names and voices using standard dialogue syntax (`Speaker1:` / `Speaker2:`).
- **Multiple Output Formats:** WAV, MP3 (128, 192, and 320 kbps), WebM/Opus, OGG, and M4A/AAC.
- **One-Click Library Transfer:** Send generated speech directly to the Audio Editor's sample library.

---

### 📝 Speech-to-Text (STT / Transcription) Studio
- Upload audio files and preview them in an integrated media player.
- Fast, high-accuracy audio transcription powered by Gemini AI models.
- One-click copy to clipboard and downloadable `.txt` transcription files.

---

### 💬 Gemini AI Chat Shortcut
- Quick navigation shortcut to open Gemini AI web chat for brainstorming and prompt design without requiring an API key.

---

### 🎚️ Multi-Track Audio Editor
The core engine packed with studio-grade capabilities:
- **Track Management:** Drag & Drop audio files, unlimited tracks, create empty tracks, per-track Mute & Lock controls.
- **Editing Tools:**
  - Split clips at playhead position (`S` key)
  - Join / merge selected clips
  - Copy, Paste, and Delete clips
  - Insert 10 seconds of silence
  - Trim clip edges non-destructively
- **Precision Control & Navigation:**
  - Live Timecode display with direct jump-to-time navigation
  - Range selection & timeline Markers
  - Zoom in/out slider with exact percentage display
  - Playback speed adjustment (0.5x to 2.0x)
  - Resizable track container height
- **Sample Library (IndexedDB):** Store audio samples locally, rename, delete, or insert them directly into the active track.
- **Auto-Save & Project State:** Real-time timeline persistence across browser refreshes, with a `Clear Timeline` button for fresh starts.
- **Advanced Export:** Render multi-track projects to WAV, MP3 (128/192/320 kbps), WebM, OGG, or M4A with live rendering progress bar and export cancellation support.

---

### 🌐 UI & Design Features
- **Bilingual Support:** Instant single-click switching between **English (LTR)** and **Persian (RTL)**.
- **Dark & Light Themes:** Toggle between modern dark and light modes with smooth CSS transitions.
- **Fully Responsive:** Optimized for desktop, tablet, and mobile browsers with touch support.

---

## 🚀 Quick Start

1. Download `audio-studio.html` (or clone this repository).
2. Open the file in any modern web browser (Chrome, Edge, Firefox, Safari).
3. Go to the **API Key** tab, paste your Google Gemini API key (obtainable from [Google AI Studio](https://aistudio.google.com/)), and click **Save Key**.
4. You are ready to go! Generate speech, transcribe audio, or mix multi-track projects.

> 💡 No `npm install`, build step, or web server setup required!

---

## 📊 Offline Capability Matrix

| Feature | Offline Status | Notes |
|---|:---:|---|
| **Audio Editor** (Import, Edit, Mix, Export WAV/WebM/M4A) | ✅ Fully Offline | Powered by browser Web Audio API |
| **Auto-Save & Sample Library** | ✅ Fully Offline | Stored locally via IndexedDB |
| **MP3 Export** | ⚠️ Online First Time | Downloads lightweight `lamejs` encoder CDN once; cached offline afterwards |
| **TTS / STT / Gemini Chat** | ❌ Online Only | Requires connection to Google Gemini API |

---

## 🛠️ Tech Stack

Built entirely in a single standalone HTML file:

- **HTML5 / CSS3:** Modern UI styled with CSS Variables, Flexbox/Grid, and hardware-accelerated animations.
- **Vanilla JavaScript (ES6+):** Dependency-free core logic.
- **Web Audio API:** High-performance real-time audio playback, mixing, processing, and offline buffer rendering.
- **IndexedDB:** Persistent client-side database for projects and media samples.
- **MediaRecorder API:** Native audio recording and container encoding.
- [**lamejs**](https://github.com/zhuker/lamejs): In-browser MP3 audio encoding.
- **Google Gemini API:** AI speech generation and audio transcription.

---

## ⌨️ Keyboard Shortcuts (Audio Editor)

| Key | Action |
|:---:|---|
| `Space` | Play / Pause playback |
| `S` | Split clip at playhead position |
| `M` | Mute / Unmute active track |
| `Delete` | Delete selected clip(s) |
| `Ctrl + Z` / `Ctrl + Y` | Undo / Redo |
| `Ctrl + C` / `Ctrl + V` | Copy / Paste clip |
| `Home` / `End` | Jump to start / end of timeline |
| `←` / `→` | Seek backward / forward 5 seconds |
| `Esc` | Deselect clips or close context menus |

---

## 🔒 Security & Privacy

- Your API Key is stored exclusively in your browser's local `localStorage`.
- All audio samples, tracks, and projects remain local inside `IndexedDB` on your device.
- The only network requests made are directly to Google Gemini API when invoking TTS/STT services and fetching the MP3 encoder script on first use.

---

## 📄 License

This project is licensed under a custom **Non-Commercial Educational License**.

- **Allowed:** Personal use, classroom/schools teaching, self-learning, modifying, and sharing free of charge.
- **Prohibited:** Any commercial use, selling the software, or incorporating it into paid products, platforms, or courses without explicit written permission.

For complete license terms, please see the [LICENSE](LICENSE) file.

For commercial licensing requests, please contact: **[Spenta-Mainyu]** ([spenta-mainyu2020@protonmail.com]).
