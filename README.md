# 🚦 Google Traffic Bot

Google Traffic Bot is a simple JavaScript tool designed to improve Google SEO by simulating organic traffic. Built with Electron for a user-friendly interface and Selenium for web automation.

---

## ✨ Features

- 🚗 **Automated Traffic Simulation:** Generate traffic to any website by simulating multiple visitors.
- 🎯 **Behavior Customization:** Define how bots interact with the site, including scrolling and clicking.
- 🌐 **Proxy Support:** Rotate through proxy servers to simulate traffic from different locations.
- 🕵️‍♂️ **Stealth Capabilities:** Include stealth settings to mimic human-like browsing and avoid bot detection mechanisms.

---

## 🛠️ Tech Stack

- **JavaScript**: Core scripting language for traffic simulation.
- **Node.js**: JavaScript runtime for executing the application.
- **Electron**: Framework for building the cross-platform desktop application.
- **Selenium**: Library for automating web browser interactions.
- **ChromeDriver**: WebDriver for controlling Chrome in Selenium.

---

## 🚨 Prerequisites

### 🖥️ Requires a Display
> ⚠️ **Note:** This application requires a display to run and **cannot run headless** for now.

### 🛑 Node.js 16 or Higher
Ensure Node.js 16 or higher is installed:

- **Windows**: Install Node.js using [Chocolatey](https://chocolatey.org/):
  ```bash
  choco install nodejs-lts
  ```

- **Ubuntu**: Install Node.js using the following commands:
  ```bash
  sudo apt update
  sudo apt install -y curl
  curl -fsSL https://deb.nodesource.com/setup_16.x | sudo -E bash -
  sudo apt install -y nodejs
  ```

### 🌟 ChromeDriver Installation
Install the version of ChromeDriver matching your Chrome browser version. For Chrome version `131`, use:
```bash
npm install chromedriver@131.0.0
```

---

## Installation (Desktop App)

### Option A: Download Ready-to-Use App (Recommended)
1. Go to [Releases](https://github.com/pavanchukkala/webtraffic/releases)
2. Download the file for your OS:
   - Windows → `WebTraffic Bot Setup 1.0.0.exe`
   - Mac → `WebTraffic Bot-1.0.0.dmg`
   - Linux → `webtraffic_1.0.0.AppImage`

### Option B: Run from Source
```bash
git clone https://github.com/pavanchukkala/webtraffic.git
cd webtraffic
npm install
mkdir -p proxy
npm start

6. Scroll to the bottom of the page → click the green button **Commit changes**

7. In the small pop-up:
   - Commit message: `Update README with easy desktop install instructions`
   - Click **Commit changes**

Done! ✅ Your README now looks professional and tells users exactly how to download the .exe etc.

---

### Now continue with Step 4 (still very easy)

**Step 4: Add Automatic Build Workflow**

1. Go to your repo: https://github.com/pavanchukkala/webtraffic

2. Click **"Add file"** → **"Create new file"**

3. In the file name box, type exactly this (including the slashes):  
   `.github/workflows/release.yml`

   (GitHub will automatically create the folders `.github` and `workflows`)

4. Paste the entire workflow code I gave you earlier into the big empty box:

```yaml
name: Build & Release Desktop App

on:
  push:
    tags:
      - "v*"

jobs:
  build:
    runs-on: ${{ matrix.os }}
    strategy:
      matrix:
        os: [windows-latest, ubuntu-latest, macos-latest]

    steps:
      - name: Checkout code
        uses: actions/checkout@v4

      - name: Setup Node.js
        uses: actions/setup-node@v4
        with:
          node-version: 20
          cache: 'npm'

      - name: Install dependencies
        run: npm ci

      - name: Build app
        run: npm run dist
        env:
          GH_TOKEN: ${{ secrets.GITHUB_TOKEN }}

      - name: Upload artifacts
        uses: softprops/action-gh-release@v2
        if: startsWith(github.ref, 'refs/tags/')
        with:
          files: |
            dist/*.exe
            dist/*.dmg
            dist/*.AppImage
            dist/*.deb

## 🛑 Disclaimer

**Google Traffic Bot** is provided for educational purposes only. 🚫 Misuse of this tool to violate any website's terms of service is not recommended or endorsed. Use responsibly!

---

## 📃 License

This project is licensed under the [MIT License](https://choosealicense.com/licenses/mit/).

---

### 🎉 Enjoy using Google Traffic Bot! 🚀
