# Athas - Windows Builds

[![Build Status](https://github.com/R4ULtv/athas-builds/actions/workflows/nightly.yml/badge.svg)](https://github.com/R4ULtv/athas-builds/actions/workflows/nightly.yml)

This repository provides automated, external **Windows builds** for the [Athas](https://github.com/athasdev/athas) lightweight code editor. Its purpose is to automatically compile the latest code from the main project and create installable packages.

> **This repository does not contain the source code for the editor itself.**
> It only contains the GitHub Actions workflows required for the build process.

---

## 🚀 Get the Latest Builds

You can find all the latest Windows builds on the [**Releases Page**](https://github.com/R4ULtv/athas-builds/releases).

Each release is tagged with the date it was built and includes:

* **Windows installer** (`.msi`)
* **Windows setup executable** (`.exe`)

---

## 📥 Installation Methods

There are **two ways** to install Athas Nightly:

### **1. Using the installer**

Download either the `.msi` or `.exe` file from the [Releases](https://github.com/R4ULtv/athas-builds/releases) page and run it.

---

### **2. Using Scoop**

Before installing, make sure you have **Microsoft Edge WebView2 Runtime** installed.
Some Windows systems already include it by default, but if not, you can download and install it from:
➡️ [Microsoft Edge WebView2 Runtime Download](https://developer.microsoft.com/it-it/microsoft-edge/webview2)

1. **Install Microsoft Visual C++ Redistributables (required)**
   Athas requires the VC++ runtime. Install it via Scoop first:

   ```powershell
   scoop bucket add extras
   scoop install extras/vcredist
   ```

2. **Install Athas Nightly**

   ```powershell
   scoop bucket add versions
   scoop install versions/athas-nightly
   ```

---

## ⚙️ How It Works

This repository uses GitHub Actions workflows to manage the process:

1. **Scheduled Trigger** – Runs nightly at midnight UTC.
2. **Fetch Latest Code** – Gets the latest commit from the `master` branch of the official [`athasdev/athas`](https://github.com/athasdev/athas) repository.
3. **Build Application** – Compiles the Tauri application for Windows and generates the installers.
4. **Create Release** – Publishes the installers to a new GitHub Release.

---

## ℹ️ About Athas

Athas is a lightweight, Tauri-based code editor. For more information, to report issues with the editor itself, or to contribute, visit:

➡️ **[github.com/athasdev/athas](https://github.com/athasdev/athas)**
