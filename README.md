# AcHDi Glassmorphism Theme for Pterodactyl 🌌

A premium, custom-built UI theme for the official Pterodactyl Panel. This theme replaces the default flat grey interface with a stunning frosted-glass aesthetic, complete with a starry night background, translucent server cards, unified navigation bars, and a glowing custom logo.

## ✨ Features
* **One-Line Installation:** Instantly download and extract the theme directly into your panel directory.
* **Frosted Glass UI:** Server cards, navigation bars, and stat boxes feature translucent blurring (`backdrop-filter`) to blend seamlessly with the background.
* **Vibrant Purple Accents:** Replaces Pterodactyl's default blue with a modern, deep purple colorway.
* **Smart Graph Transparency:** Completely overrides opaque graph backgrounds on the server management view.
* **Glowing Branding:** Replaces the default panel text font with **Montserrat** and adds an interactive neon purple glow.

---

## 🛠️ Prerequisites
Before installing this theme, ensure your server meets the following requirements:
* A fully installed, official **Pterodactyl Panel**.
* Root SSH access to your web server.
* Node.js and `yarn` installed on your panel server.

---

## 🚀 Installation Guide

Log into your web server via SSH as `root`. You can copy the entire block below and paste it directly into your terminal. It will automatically run through every step of the installation!

```bash
# 1. Navigate to your Pterodactyl installation directory
# (If you installed Pterodactyl in a custom location, change this path)
cd /var/www/pterodactyl

# 2. Download the theme directly from GitHub and extract it.
# The --strip-components=1 flag ensures the files overwrite the defaults perfectly.
curl -L https://github.com/achdiop/Pterodactyl-UI/archive/refs/heads/main.tar.gz | tar -xzv --strip-components=1

# 3. Update and install any necessary Node.js dependencies
yarn

# 4. Set the legacy OpenSSL provider (required for newer Node versions) 
# and build the production assets for the panel to apply the CSS changes.
# Note: This may take a few minutes to complete!
export NODE_OPTIONS=--openssl-legacy-provider
yarn build:production

# 5. Clear the application caches so the new theme registers immediately
php artisan view:clear
php artisan config:clear

# 6. Ensure the correct permissions are set for the webserver
# (Replace www-data:www-data with nginx:nginx or apache:apache if on CentOS/AlmaLinux)
chown -R www-data:www-data /var/www/pterodactyl/*
