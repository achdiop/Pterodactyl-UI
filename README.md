# AcHDi Glassmorphism Theme for Pterodactyl 🌌

A premium, custom-built UI theme for the official Pterodactyl Panel. This theme replaces the default flat grey interface with a stunning frosted-glass aesthetic, complete with a starry night background, translucent server cards, unified navigation bars, and a glowing custom logo.

## ✨ Features
* **Drop-in Installation:** Pre-configured files that extract perfectly into your panel directory.
* **Frosted Glass UI:** Server cards, navigation bars, and stat boxes feature translucent blurring (`backdrop-filter`) to blend seamlessly with the background.
* **Vibrant Purple Accents:** Replaces Pterodactyl's default blue with a modern, deep purple colorway.
* **Smart Graph Transparency:** Completely overrides opaque graph backgrounds on the server management view.
* **Glowing Branding:** Replaces the default panel text font with **Montserrat** and adds an interactive neon purple glow.

---

## 🛠️ Prerequisites
Before installing this theme, ensure your server meets the following requirements:
* A fully installed, official **Pterodactyl Panel**.
* Root SSH access to your web server.
* `yarn` and `node` installed on your panel server.

---

## 🚀 Installation Guide

### 1. Download and Extract the Theme
Log into your web server via SSH as `root`. Navigate to your Pterodactyl directory, download the theme archive, and extract it to overwrite the default configuration files.

Run the following commands:

```bash
cd /var/www/pterodactyl
curl -L -o achdi-theme.tar.gz [https://raw.githubusercontent.com/YOUR_USERNAME/YOUR_REPO/main/achdi-theme.tar.gz](https://raw.githubusercontent.com/YOUR_USERNAME/YOUR_REPO/main/achdi-theme.tar.gz)
tar -xzvf achdi-theme.tar.gz
