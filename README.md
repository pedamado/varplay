# VarPlay – Variable Font Playground

**VarPlay** is a brutalist, client-side sandbox for testing, exploring, and validating variable font files (`.ttf`, `.otf`, `.woff2`).

> Designed for type design students and professionals, it combines technical inspection with playful typographic experimentation in a single, distraction-free interface.

---

## 🚀 Quick Start

### Running Locally
Because this application uses modern web features (Service Workers) and fetches local resources, **it requires a local server to run correctly**. Simply opening `index.html` via double-click may cause CORS errors.

1.  **Download** the files into a folder named `VarPlay`.
2.  **Open your terminal** or command prompt in that folder.
3.  **Run a simple server** using one of the methods below:

    * **Python 3:**
        ```bash
        python3 -m http.server
        ```
    * **Node/NPM:**
        ```bash
        npx serve
        ```
    * **VS Code:**
        Use the **"Live Server"** extension.

4.  Open your browser to `http://localhost:8000` (or the port shown in your terminal).

---

## ✨ Features

### 1. Drag & Drop Testing
* Drop any variable font file directly onto the window.
* **Format Support:** `.ttf`, `.otf`, and `.woff2`.
* **Privacy First:** All processing happens locally in your browser. No font files are uploaded to any server.

### 2. Live Metadata Inspector (`INFO` Tab)
Instantly view crucial file metadata often hidden in design software:
* **Metrics:** UPM, Glyph Count, Ascender/Descender (Typo & Win), Line Gap, X-Height, Cap Height.
* **Legal:** License, Designer, Copyright, and Embedding Permissions (`fsType`).
* **Instances:** Dropdown list of all named instances (e.g., "Bold Condensed") found in the font.

### 3. Variable Axis Controls (`VARS` Tab)
* **Auto-detection:** Automatically detects all registered axes (Weight, Width, Slant, Optical Size, etc.).
* **Animation:** Play/Pause animations for individual axes or all at once.
* **Speed & Easing:** Control playback speed (0.25x to 4x) and toggle between Linear and Sine-wave easing.

### 4. Advanced Text Tools (`TEXT` Tab)
* **Preset Content:** Quick access to A-Z, numbers, and multi-language Pangrams.
* **Kerning Pairs:** Specialized strings for testing spacing (e.g., `AV`, `To`, `T.`).
* **Adhesion Generator:** Generates dummy words using *only* the characters you input. Perfect for testing fonts with limited character sets during development.

### 5. OpenType Features (`FEAT` Tab)
One-click toggles for common OpenType features, categorized by:
* **Ligatures**
* **Figures** (Oldstyle, Tabular)
* **Positioning** (Superscript)
* **Alternates** (Swashes, Stylistic Sets)

### 6. Atomic Effects (`EFFX` Tab)
* **Filters:** Apply CSS blur to simulate bad printing or low-res screens.
* **Geometry:** Mirror text X or Y.
* **Atomic Randomizer:** Apply variable axis changes per **Glyph** or **Word**. Create "waves" of weight, random widths, or inverse bell curves across your text string.

---

## 🛠 Project Structure

* `index.html`: The core application containing HTML structure, Tailwind CSS classes, and the main JavaScript logic (font parsing, UI interaction).
* `settings.js`: Configuration file containing app metadata, pangram lists, and kerning pairs.
* `manifest.json`: Web App Manifest allowing VarPlay to be installed as a desktop application (PWA).
* `sw.js`: Service Worker for offline caching capabilities.

---

## 📜 License & Credits

* **Author:** Pedro Amado (FBAUP / i2ADS / Ligatures SIG) & Gemini Pro 3.0.
* **Date:** November 25, 2025.
* **Version:** 1.1
* **License:** MIT / Creative Commons Attribution-ShareAlike 4.0 International.

### Credits
Developed from original concepts found in:
* **Font Gauntlet** by Dinamo Foundry
* **Adhesion Text** by Miguel Sousa
* **HAL Type Pad** by Han Li

**Fonts:**
* **Inter** by Rasmus Andersson (Google Fonts)
