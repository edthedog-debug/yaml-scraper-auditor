<div align="center">

  <img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=6,11,20,30,45&height=180&section=header&text=YAML%20Scraper%20&%20LLM%20Auditor&fontSize=32&fontColor=ffffff&fontAlignY=38&desc=Client-Side%20Pipeline%20Automation%20&%20Local-First%20File%20Sync&descSize=14&descAlignY=62" width="100%" />

  <p>
    <em>A high-density, client-side YAML pipeline engine for automated web extraction, local directory synchronization, and structured auditing.</em>
  </p>

  <p>
    <img src="https://img.shields.io/badge/Status-Active%20Development-00ff66?style=for-the-badge&logo=codeforces&logoColor=00ff66" alt="Status" />
    <img src="https://img.shields.io/badge/License-MIT-blue?style=for-the-badge&logo=opensourceinitiative&logoColor=white" alt="License" />
    <img src="https://img.shields.io/badge/Platform-GitHub%20Pages-orange?style=for-the-badge&logo=github&logoColor=white" alt="GitHub Pages" />
    <img src="https://img.shields.io/badge/Storage-File%20System%20API-purple?style=for-the-badge&logo=googlechrome&logoColor=white" alt="Local First" />
  </p>

  <p>
    <a href="#-features"><strong>Features</strong></a> ·
    <a href="#-live-demo"><strong>Live Demo</strong></a> ·
    <a href="#-quick-start"><strong>Quick Start</strong></a> ·
    <a href="#-yaml-schema"><strong>YAML Schema</strong></a> ·
    <a href="#-architecture"><strong>Architecture</strong></a>
  </p>

</div>

---

## ⚡ Overview

**YAML Scraper & LLM Auditor** is a zero-backend, client-side developer utility engineered for executing data extraction and transformation pipelines directly inside the browser. It combines a rigorous code-auditor aesthetic with modern web APIs (`File System Access API`, `Web Workers`, and background cron schedulers) to run robust automation tasks without exposing server endpoints or requiring complex backend infrastructure.

---

## 🚀 Key Features

* **YAML Pipeline Definition:** Configure target URLs, CSS selectors, extraction attributes, and LLM normalization rules using a lightweight YAML specification.
* **Local-First Directory Sync:** Leverages the browser's native **File System Access API** to automatically commit and write scraped datasets directly to a designated local folder on your hard drive.
* **Background Cron Scheduler:** Keep the dashboard open in the background to trigger automated audit cycles hourly, daily at 21:00 UTC, weekly, or on custom intervals.
* **Live Audit Terminal & Progress Tracker:** Real-time visual progress bar tracking execution phases (*DOM Fetch, Extraction, Normalization, File I/O*) paired with an animated developer log window.
* **Audit Report Generator:** Instantly compile execution logs, YAML configs, and extracted payloads into downloadable `.txt` audit reports.

---

## 🖥️ Live Demo

You can try the fully functional web application instantly via GitHub Pages:

👉 **[Launch YAML Scraper & LLM Auditor Live](https://YOUR_GITHUB_USERNAME.github.io/YOUR_REPOSITORY_NAME/)**  
*(Replace `YOUR_GITHUB_USERNAME` and `YOUR_REPOSITORY_NAME` with your actual GitHub details)*

---

## 🛠️ Quick Start

Because this tool runs entirely client-side inside a single robust architecture, you don't need `npm install`, complex build scripts, or Docker containers to run it.

1. **Clone the repository:**
   ```bash
   git clone [https://github.com/YOUR_GITHUB_USERNAME/YOUR_REPOSITORY_NAME.git](https://github.com/YOUR_GITHUB_USERNAME/YOUR_REPOSITORY_NAME.git)
   cd YOUR_REPOSITORY_NAME
