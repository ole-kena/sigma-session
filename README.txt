# Sigma Session — Android-ready web app

This is an installable Progressive Web App (PWA), not a signed APK yet.

## Install on Android
1. Upload/extract this folder to a static HTTPS host (for example GitHub Pages, Netlify, or your own website).
2. Open the HTTPS site in Chrome on your Android phone.
3. Open Chrome menu (⋮) and choose **Install app** or **Add to Home screen**.
4. Launch **Sigma Session** from your app drawer.

A PWA needs HTTPS (or localhost) for service workers and installation. Opening index.html directly from Files will show the dashboard, but offline caching and installation will not work.

## Features
- Local live clock and date
- Tokyo, London, and New York session status
- Automatic time-zone/DST conversion via IANA time zones
- ICT killzone display using New York local time
- 12/24-hour setting
- Basic browser session-open notifications while the app is running

## Important
Session windows are reference hours, not broker-specific market hours. Browser notifications may not fire reliably when Android suspends the app. A future native Android build can add reliable scheduled notifications.
