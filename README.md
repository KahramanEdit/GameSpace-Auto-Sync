<div align="center">

# 🎮 GameSpace Auto Sync
### Never lose your Game Space library again.

[![Android](https://img.shields.io/badge/Android-11%2B-green?style=for-the-badge&logo=android)](https://www.android.com/)
[![LSPosed](https://img.shields.io/badge/LSPosed-Module-blue?style=for-the-badge)](https://github.com/LSPosed/LSPosed)
[![Root](https://img.shields.io/badge/Root-Magisk%20%7C%20KernelSU-orange?style=for-the-badge)](https://github.com/topjohnwu/Magisk)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow?style=for-the-badge)](https://opensource.org/licenses/MIT)

An LSPosed module designed for **Nubia / RedMagic** devices to automatically backup, restore, and manage your Game Space (`cn.nubia.gamelauncher`) library.

[Features](#-features) • [Requirements](#-requirements) • [Installation](#-installation-guide) • [Disclaimer](#-disclaimer--liability)

</div>

---

## 📖 The Problem
If you use root (Magisk/KernelSU), you might occasionally boot into **Safe Mode** due to a bad module or system crash. When this happens, the Nubia Game Space application resets its database, wiping all your manually added games. You are then forced to manually re-add dozens of games one by one.

## 💡 The Solution
This module hooks into the Game Space database and creates a secure backup of your selected games. 
1. **Auto-Restore:** Every time Game Space opens, the module checks if your games are missing. If the database was wiped (e.g., after Safe Mode), it instantly restores them.
2. **Companion App:** It includes a standalone APK (GameSpace Sync) with a clean UI. You can see all your installed apps, and with a single tap, force-add non-game apps (like emulators, video editors, or specific tools) into Game Space.
3. **Instant Apply:** When you toggle an app in the UI, the module automatically force-stops Game Space in the background so your changes apply immediately the next time you open it.

## ✨ Features
- **Native Filtering:** Relies purely on Nubia's native `isGame` flag. No hardcoded package names or annoying bloatware.
- **Safe Mode Protection:** Automatically restores your game list even if the system wipes the Game Space data.
- **Manual Override:** Add any app (e.g., CapCut, Termux) to Game Space using the companion app.
- **Smooth UI:** Check/uncheck apps without the list jumping back to the top.
- **No Magisk Modules Required:** Completely runs within LSPosed.

## 📱 Requirements
- **Root** (Magisk / KernelSU / APatch)
- **LSPosed** (Zygisk or Vector)
- A Nubia / RedMagic device running Nubia UI / RedMagic OS (Target package: `cn.nubia.gamelauncher`)
- Android 11+ (Tested on Android 16)

## 🚀 Installation Guide

1. **Download & Install:** Go to the [Releases](../../releases) tab and download the latest `GameSpaceSync_vX.X.apk`. Install it on your device.
2. **Enable in LSPosed:** 
   - Open the LSPosed Manager.
   - Go to **Modules** and enable **GameSpace Sync**.
   - Tap on the module and ensure the **Scope** is set to only `cn.nubia.gamelauncher` (Game Space).
3. **Reboot:** Reboot your device so LSPosed can load the module.
4. **Grant Root:** Open the **GameSpace Sync** app from your app drawer. Grant root permissions when prompted (required to read/write the Game Space database).
5. **Done!** You can now manually toggle apps in the list. Your game list will now be backed up and auto-restored forever.

## ⚠️ Disclaimer & Liability
- **Use at your own risk.**
- This module modifies the database of a system application (`cn.nubia.gamelauncher`). While it has been thoroughly tested, root modifications can sometimes lead to bootloops, data loss, or unexpected behavior.
- The developer is **not responsible** for bricked devices, wiped data, or any damage caused to your device.
- It is highly recommended to have a recent backup of your device (e.g., TWRP/Nandroid backup) before using any system-level modifications.
- This project is not affiliated with Nubia, ZTE, or RedMagic.

## 👨‍💻 Author
**Clenix / Kahraman**
- Feel free to open an issue if you encounter any bugs or have feature requests!

---
<div align="center">
If this module saved you from the pain of manually re-adding your games, feel free to give the repo a ⭐!
</div>
