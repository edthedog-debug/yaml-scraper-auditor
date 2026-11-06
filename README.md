<div align="center">

  <img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=6,11,20,30,45&height=180&section=header&text=YAML%20Scraper%20&%20AI%20Pipeline&fontSize=32&fontColor=ffffff&fontAlignY=38&desc=Client-Side%20Regex%20&%20Custom%20LLM%20Auditing%20Engine&descSize=14&descAlignY=62" width="100%" />

  <p>
    <em>An industrial, high-density client-side YAML pipeline engine featuring local Regex parsing, custom AI endpoint integration, local directory syncing, and advanced cron scheduling.</em>
  </p>

  <p>
    <img src="https://img.shields.io/badge/Status-Active%20Deployment-10b981?style=for-the-badge&logo=codeforces&logoColor=10b981" alt="Status" />
    <img src="https://img.shields.io/badge/License-MIT-blue?style=for-the-badge&logo=opensourceinitiative&logoColor=white" alt="License" />
    <img src="https://img.shields.io/badge/Platform-GitHub%20Pages-orange?style=for-the-badge&logo=github&logoColor=white" alt="GitHub Pages" />
    <img src="https://img.shields.io/badge/Engine-Regex%20%2B%20Custom%20LLM-cyan?style=for-the-badge&logo=openai&logoColor=white" alt="Engine" />
  </p>

  <p>
    <a href="#-features"><strong>Features</strong></a> ·
    <a href="#-quick-start"><strong>Quick Start</strong></a> ·
    <a href="#-ai-integration-tutorial"><strong>AI Setup Tutorial</strong></a> ·
    <a href="#-user-manual"><strong>User Manual</strong></a> ·
    <a href="#-yaml-schema"><strong>YAML Schema</strong></a>
  </p>

</div>

---

## ⚡ Overview

**YAML Scraper & AI Pipeline** is a zero-backend, browser-native developer tool built with an industrial **Iron & Raw Steel** aesthetic. It allows you to run robust scraping pipelines using either **Local Regex DOM Parsing** (fast, private, offline) or a **Custom AI API Endpoint** (OpenAI, Gemini, or self-hosted LLMs) for semantic data structuring. 

Combined with native browser folder syncing via the **File System Access API** and a granular cron scheduler, it can run autonomously in the background while you work.

---

## 🚀 Key Features

* **Dual-Engine Architecture:** Choose between ultra-fast **Local Regex** (default, no API key needed) or connect any **Custom AI Endpoint** for intelligent data extraction.
* **Granular Cron Scheduler:** Set automated execution triggers specifying exact days of the week, hours, and minutes.
* **Local Directory Sync:** Leverages the native **File System Access API** to automatically commit scraped JSON payloads directly to a chosen folder on your local disk.
* **Industrial Dev UI:** High-density dark theme (`#07090c`), tactical borders, matrix green accents, and a real-time audit terminal.
* **Audit Report Generator:** Instantly compile logs, YAML configurations, and extracted datasets into downloadable `.txt` or `.json` reports.

---

## 🛠️ Quick Start

1. Clone or download this repository.
2. Ensure `index.html` is in the root directory.
3. Push to your repository and enable **GitHub Pages** under repository `Settings > Pages` (Source: `main` branch, `/root`).
4. Open your public GitHub Pages URL in any modern browser (Chrome, Edge, Opera).

---

## 🤖 AI Integration Tutorial

By default, the engine runs entirely offline using **Local Regex & DOM selectors**. If you want to enable advanced semantic AI extraction using your own LLM provider (OpenAI, Google Gemini, Anthropic, or Local LLM via Ollama/LM Studio), follow these steps:

1. **Open the Application:** Navigate to your hosted GitHub Pages link.
2. **Access the Configuration Panel:** Look at the left sidebar and click on the **AI / LLM Endpoint** tab.
3. **Configure Your Provider:**
   * **Engine Selector:** Switch from *Local Regex (Offline)* to **Custom AI Endpoint (LLM)**.
   * **API Base URL:** Enter your provider's endpoint URL.
     * *OpenAI Example:* `https://api.openai.com/v1/chat/completions`
     * *Gemini API Example:* `https://generativelanguage.googleapis.com/v1beta/models/gemini-1.5-flash:generateContent?key=YOUR_KEY`
     * *Local Ollama Example:* `http://localhost:11434/v1/chat/completions`
   * **Model Identifier:** Type the model name (e.g., `gpt-4o-mini`, `gemini-1.5-flash`, `llama3`).
   * **Secret API Key:** Paste your private API key. *(Note: Keys remain 100% client-side in your browser memory and are never stored externally).*
4. **Test & Run:** Modify your YAML pipeline to include a transformation prompt, then click **EXECUTE NOW** to watch the AI normalize and structure the scraped data.

---

## 📖 User Manual & Operational Guide

### 1. YAML Pipeline Spec Editor
Located on the left panel under the **YAML Pipeline** tab. Here you define your scraping rules using clean YAML syntax:
* `target_url`: The website URL to scrape.
* `extraction_rules`: Define container classes, CSS selectors, and target attributes.
* `llm_transformation`: Optional instructions for the AI parser to categorize, clean, or format the extracted records.

### 2. Scheduler & Local Storage Setup
Switch to the **Scheduler & Storage** tab to configure automation:
* **Local Folder Auto-Save:** Click **Set Destination Directory** and grant browser permission to a local folder. Every time the pipeline runs, a timestamped `.json` file will be written directly to your computer.
* **Granular Cron Scheduler:** 
  * Check the specific days of the week you want the task to run (e.g., Monday, Wednesday, Friday).
  * Set the exact hour (00-23) and minute (00-59).
  * Keep the browser tab open in the background; the live countdown timer will trigger executions automatically.

### 3. Execution & Monitoring
* **Live Audit Terminal:** Displays real-time status updates, HTTP fetch diagnostics, parsing events, and success/error codes with timestamped logs.
* **Progress Bar:** Tracks the execution lifecycle: `PARSING_YAML_SPEC` ➔ `HTTP_FETCH_DOM` ➔ `EXTRACTING_NODES` ➔ `AI_NORMALIZATION` ➔ `WRITING_LOCAL_FILE`.
* **Exporting Reports:** Use the **Download Full TXT Report** button to generate a complete audit trail containing the exact YAML configuration, terminal logs, and structured JSON results.

---

## 📄 Example YAML Pipeline Schema

```yaml
version: "2.0.0"
pipeline_meta:
  name: "Industrial Tech Feed Auditor"
  engine: "regex" # or "llm"
targets:
  - url: "[https://news.ycombinator.com](https://news.ycombinator.com)"
    selectors:
      - item: "tr.athing"
        fields:
          title: "span.titleline > a"
          link: "span.titleline > a [href]"
output:
  format: "json"
  auto_save_local: true
