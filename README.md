# Athas - Windows Builds

[![Build Status](https://github.com/R4ULtv/athas-builds/actions/workflows/nightly.yml/badge.svg)](https://github.com/R4ULtv/athas-builds/actions/workflows/nightly.yml)

This repository provides automated, external builds for the [Athas](https://github.com/athasdev/athas) lightweight code editor. Its purpose is to automatically compile the latest code from the main project and create installable packages for various operating systems.

> **This repository does not contain the source code for the editor itself.** It only contains the GitHub Actions workflows required for the build process.

## 🚀 Get the Latest Builds

You can find all the latest builds on the [**Releases Page**](https://github.com/R4ULtv/athas-builds/releases).

Each release is tagged with the date it was built and includes installers for:
*   **Windows** (`.msi`, `.exe`)

## How It Works

This repository uses a set of GitHub Actions workflows to manage the entire process:

1.  **Scheduled Trigger:** A workflow runs every night at midnight (UTC).
2.  **Fetch Latest Code:** It identifies the latest commit on the `master` branch of the official `athasdev/athas` repository.
3.  **Build Application:** A reusable workflow compiles the Tauri application for Windows creating the necessary installers.
4.  **Create Release:** Once the builds are complete, another workflow publishes them to a new GitHub Release, making them available for download.

## About Athas

Athas is a lightweight, Tauri-based code editor. For more information, to report issues with the editor itself, or to contribute, please visit the official repository:

➡️ **[github.com/athasdev/athas](https://github.com/athasdev/athas)**
