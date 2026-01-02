# Gemini CAT Tool (Client-Side) 🐱

A powerful, single-file browser-based translation tool powered by **Google Gemini models**. Designed specifically to solve layout issues in PPTX translations, such as vertical text fragmentation and font expansion.

![Version](https://img.shields.io/badge/version-14.2-blue.svg)
![License](https://img.shields.io/badge/license-MIT-green.svg)

## ✨ Key Features

* **📄 Smart Layout Saver**: 
    * **Vertical Text Fix**: Intelligently merges fragmented vertical text (e.g., "服", "務") into coherent words before translation.
    * **Auto-Fit for Japanese**: Automatically shrinks font size by 15% when translating CJK to Japanese to prevent text overflow.
* **🤖 Context-Aware Polishing**: Uses a sliding window approach to read surrounding sentences, ensuring the translation flows naturally like a human editor.
* **🎨 SmartArt Support**: Deep parsing of PPTX SmartArt diagrams (direct access to `data*.xml`), which most basic tools miss.
* **🔒 Privacy Focused**: 
    * **Client-Side Only**: No backend server. Your files are processed locally in your browser.
    * **Direct API Call**: Your API Key is sent directly from your browser to Google's servers.
* **⚡ Model Auto-Switching**:
    * Prioritizes **Gemini 2.0 Flash (Exp)** for speed.
    * Automatically falls back to **Gemini 2.5 Flash** if the rate limit is hit.

## 🚀 How to Use

1.  **Download**: Save the `index.html` file from this repository to your computer.
2.  **Open**: Double-click `index.html` to open it in Chrome, Edge, or Safari.
3.  **Setup**:
    * Enter your [Google Gemini API Key](https://aistudio.google.com/app/apikey).
    * Select Source and Target languages.
4.  **Translate**:
    * **Step 1**: Load & Parse your file (`.pptx`, `.docx`, `.xlsx`, `.txt`).
    * **Step 2**: Click **初步翻譯 (Translate)**.
    * **Step 3 (Optional)**: Click **深度潤稿 (Polish)** for context-aware refinement.
    * **Step 4**: Download the translated file.

## 🛠️ Supported Formats

* **PPTX**: Advanced support (SmartArt, Tables, Shapes, Grouped Objects).
* **DOCX**: Paragraph processing.
* **XLSX**: Shared strings translation.
* **TXT**: Line-by-line translation.

## ⚠️ Requirements

* A valid Google Gemini API Key.
* A modern web browser (Chrome/Edge recommended).
* Internet connection (to reach Google APIs).

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---
*Created to solve the pain of PPT translation.*
