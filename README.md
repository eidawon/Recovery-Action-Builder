# Android Custom Recovery Builder

[![License: Apache-2.0](https://img.shields.io/badge/license-Apache%202.0-blue.svg)](LICENSE)

A fully automated recovery image builder for **Custom Recoveries** using GitHub Actions. Designed to support AOSP-based recovery projects including forked or personal implementations.

---

## ✅ Features

- Supports build targets: `boot`, `recovery`, and `vendor_boot`
- Generates raw `.img` files (suitable for fastboot flashing)
- Auto-upload to GitHub Releases
- Works with **private device trees** via PAT (`RECOVERY` secret)
- Optional build types: `eng`, `userdebug`, `user`
- Includes **LDCheck** for blob dependency validation
- Post-build cleanup to conserve GitHub Actions storage

---

## 🚀 Getting Started

1. **Fork or clone** this repository.
2. Copy the desired workflow(s) into `.github/workflows/`.
3. In your repository settings, add the following GitHub Secret:
   - `RECOVERY` – A **GitHub Personal Access Token (PAT)** with `repo` permissions (required for private repos)
4. Manually trigger the build:
   - Go to **Actions** tab → Select workflow → **Run workflow**
   - Fill out required inputs such as manifest branch, device tree URL, and codename

---

## 📦 Output

- Raw image:  
  - `recovery.img`, `boot.img`, or `vendor_boot.img`
- Tagged GitHub Release containing the image and build metadata

---

## 🙌 Credits

- [@azwhikaru](https://github.com/azwhikaru) – Base workflow template
- [@carlodandan](https://github.com/carlodandan) – CI build system inspiration
- [TeamWin](https://github.com/TeamWin), [OrangeFox](https://gitlab.com/OrangeFox) – Recovery maintainers
- All open-source contributors, testers, and Android modders

---

## ⚠️ Disclaimer

This is a **community-driven project** and is not affiliated with any official recovery team or OEM.  
Use at your own risk. Always validate builds before flashing.  
Respect all licenses and give credit where due.

---

## 📜 License

Licensed under the [Apache License 2.0](LICENSE).
