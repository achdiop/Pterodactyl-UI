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

### 1. Download and Apply the Theme Files
Log into your web server via SSH as `root`. The following command block will navigate to your Pterodactyl directory, download this repository as a ZIP file, extract the `tailwind.config.js` and `resources` folders to overwrite the defaults, and clean up the downloaded files.

Copy and paste this entire block into your terminal:

```bash
cd /var/www/pterodactyl

# Ensure unzip is installed on your server
apt update && apt install -y unzip

# Download the repository as a ZIP file
curl -L -o achdi-theme.zip https://github.com/achdiop/Pterodactyl-UI/archive/refs/heads/main.zip

# Extract into a temporary folder and copy the files to the root directory
unzip -q -o achdi-theme.zip -d achdi_temp
cp -rf achdi_temp/*/* ./

# Clean up the downloaded zip and temporary folder
rm -rf achdi_temp achdi-theme.zip
