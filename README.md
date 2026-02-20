# 🚦 WebTraffic Bot

**WebTraffic Bot** is a powerful desktop application that simulates real organic traffic to any website. Built with Electron + Selenium, it helps with SEO testing by generating visits from different locations using proxies.

---

## ✨ Features
- 🚗 **3 Traffic Modes**: Direct, Google Search + Click, Proxy Rotation
- 🌐 **Proxy Support**: Drop your proxy list in `/proxy/` folder (one per line)
- 🕵️‍♂️ **Stealth Mode**: Hides automation flags to look more human
- 📈 **Auto Scroll & Interaction**: Realistic page behavior
- 🎨 **Simple GUI**: Easy to use interface with Start/Stop buttons

---

## 🛠️ Tech Stack
- **Electron** — Cross-platform desktop app
- **Selenium + ChromeDriver** — Browser automation
- **Node.js** — Backend logic
- **jQuery** — UI interactions

---

## 📦 Installation

### Option A: Download Ready-to-Use App (Recommended)
1. Go to **[Releases](https://github.com/pavanchukkala/webtraffic/releases)**
2. Download the file for your operating system:
   - **Windows** → `WebTraffic Bot Setup 1.0.0.exe`
   - **Mac** → `WebTraffic Bot-1.0.0.dmg`
   - **Linux** → `webtraffic_1.0.0.AppImage`

### Option B: Run from Source
```bash
git clone https://github.com/pavanchukkala/webtraffic.git
cd webtraffic
npm install
mkdir -p proxy
npm start

🛑 Prerequisites

Node.js 16 or higher
Google Chrome installed (version matching chromedriver 131)
For Linux headless (optional): sudo apt install xvfb


🛑 Disclaimer
This tool is for educational and testing purposes only.
Misuse on live websites may violate their Terms of Service. Use responsibly!

📃 License
MIT License © pavanchukkala

Enjoy generating traffic! 🚀
Made with ❤️ by pavanchukkala
text---

### Next Step (Quick)
1. Go to your repo
2. Click **"Add file" → "Create new file"**
3. Name: `.github/workflows/release.yml`
4. Paste the workflow code I gave earlier (the long YAML)
5. Commit it

After you update these two files + the workflow, just reply **“Done”** and I’ll tell you exactly how to create the release that builds your `.exe` automatically.

You’re literally 2 minutes away from having professional downloadable builds!  
Copy → Paste → Commit. Let’s go! 🚀
