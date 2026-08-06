# 🎬 Subtitle Tools — Client-Side Subtitle Processing Suite

[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![Privacy: 100% Client-Side](https://img.shields.io/badge/Privacy-100%25%20Client--Side-blue.svg)](#-privacy--security)
[![Powered By WebAssembly](https://img.shields.io/badge/Powered%20By-FFmpeg.wasm-orange.svg)](#-included-tools)
[![GitHub Pages Compatible](https://img.shields.io/badge/Deploy-GitHub%20Pages-brightgreen.svg)](#-hosting-on-github-pages)

A modern, fast, and **100% private** web-based suite of tools for merging, encoding, converting, and extracting video subtitles directly inside your browser. No server uploads, no privacy risks, zero external dependencies required.

---

## 🌟 Key Highlights

- **🔒 100% Private & Serverless**: All processing (parsing, character encoding conversion, FFmpeg demuxing) happens locally on your computer. Your files never touch any external server.
- **⚡ Instant & Offline Capable**: Zero download queues or server processing delays. Works offline once loaded.
- **🎨 Sleek Modern UI**: Dark-mode interface designed with modern aesthetics and responsive layout for all devices.
- **🚀 Zero Installation**: Open `.html` files directly in any web browser or host on GitHub Pages with 1 click.

---

## 🛠️ Included Tools

### 1. 🔀 Subtitle Merger (`index.html`)
Combine two different subtitle files (e.g., English + Turkish) into a single dual-language subtitle file for language learning or bilingual viewing.
- **Top / Bottom Placement**: Assign primary subtitle to bottom and secondary to top of the screen.
- **Time Offset Sync**: Adjust timing shifts (+/- seconds or milliseconds) for perfect audio sync.
- **Style Customization**: Customize font colors, sizes, and backgrounds for both subtitle tracks.

### 2. 🔀 UTF-8 Converter & Format Transformer (`convert.html`)
Fix garbled non-ASCII characters (e.g., Turkish `ğ, ş, ı, İ, ç, ö, ü`, Cyrillic, Greek, CJK) caused by legacy encodings.
- **Automatic & Manual Encoding Fix**: Convert legacy encodings (`Windows-1254`, `ISO-8859-9`, `ISO-8859-1`, `Windows-1252`, `UTF-16`) to standard `UTF-8`.
- **Format Conversion**: Convert between `.srt`, `.vtt`, `.ass`, and plain `.txt`.
- **Batch Processing**: Convert multiple subtitle files simultaneously.

### 3. 🎥 Video Subtitle Extractor (`extract.html`)
Extract embedded soft subtitles directly from `.mkv`, `.mp4`, `.webm`, or `.avi` video files in your browser.
- **Powered by FFmpeg WebAssembly**: Uses WebAssembly to demux media files inside your browser.
- **Track Selection**: Detects all embedded audio/subtitle tracks and lets you export selected tracks to `.srt` or `.vtt`.
- **No File Size Upload Limits**: Processes large video files locally without consuming network bandwidth.

---

## 🚀 Quick Start / How to Run

### Option A: Open Directly in Browser (Local)
1. Clone or download this repository:
   ```bash
   git clone https://github.com/YOUR_USERNAME/subtitle-tools.git
   ```
2. Double-click `index.html` (or `convert.html`, `extract.html`) to open it directly in your web browser.

### Option B: Hosting on GitHub Pages (Free)
1. Upload this repository to GitHub.
2. In your repository on GitHub, go to **Settings** -> **Pages**.
3. Under **Build and deployment** -> **Branch**, select `main` (or `master`) and `/ (root)`.
4. Click **Save**. Your site will be live at `https://YOUR_USERNAME.github.io/subtitle-tools/` in seconds!

---

## 🔒 Privacy & Security

Most online subtitle converters and extractors require uploading video and subtitle files to remote servers. **Subtitle Tools** operates entirely within the browser sandbox using HTML5 File APIs, TextDecoder/TextEncoder, and WebAssembly (`ffmpeg.wasm`). No network requests containing your file data are ever sent.

---

## 📁 Repository Structure

```
Subtitle-Tools/
├── index.html        # Subtitle Merger tool
├── convert.html      # UTF-8 Encoding Converter & Format Transformer
├── extract.html      # Video Subtitle Extractor (FFmpeg.wasm)
├── LICENSE           # MIT License
├── README.md         # Project Documentation
├── CONTRIBUTING.md   # Guidelines for contributors
└── .github/          # Issue templates & repository configs
    └── ISSUE_TEMPLATE/
        ├── bug_report.md
        └── feature_request.md
```

---

## 📄 License

Distributed under the MIT License. See [`LICENSE`](LICENSE) for more information.
