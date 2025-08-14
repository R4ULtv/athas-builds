# Athas - Windows Builds

[![Build Status](https://github.com/R4ULtv/athas-builds/actions/workflows/nightly.yml/badge.svg)](https://github.com/R4ULtv/athas-builds/actions/workflows/nightly.yml)

This repository provides automated, external **Windows builds** for the [Athas](https://github.com/athasdev/athas) lightweight code editor. Its purpose is to automatically compile the latest code from the main project and create installable packages.

> **This repository does not contain the source code for the editor itself.**
> It only contains the GitHub Actions workflows required for the build process.

---

## 🚀 Get the Latest Builds & Installation

You can find all the latest Windows builds on the [**Releases Page**](https://github.com/R4ULtv/athas-builds/releases).

Each release is tagged with the date it was built and includes multiple installation options:

### **📦 Complete Setup (Recommended)**

**Files**: `Athas_{version}-setup.exe` or `Athas_{version}_x64_en-US.msi`

These installers include **everything built-in**:
- Microsoft WebView2 Runtime
- Visual C++ Redistributables
- Complete standalone installation

Simply download and run either file from the [Releases](https://github.com/R4ULtv/athas-builds/releases) page - no additional setup required.

---

### **🪣 Scoop Package Manager**

**For advanced users** who prefer package management:

```powershell
scoop bucket add versions
scoop install versions/athas-nightly
```

**Important**: The Scoop version is a **standalone build** that requires manual setup of dependencies:

1. **Install Microsoft Visual C++ Redistributables**:
  ```powershell
  scoop bucket add extras
  scoop install extras/vcredist
  ```

2. **Install Microsoft WebView2 Runtime** (if not already present):
  Download from [Microsoft WebView2 Runtime](https://developer.microsoft.com/it-it/microsoft-edge/webview2)

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
