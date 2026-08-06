# NetWatch

**NetWatch** is a lightweight, offline-first Windows desktop app for network monitoring — network adapters, live internet speed, IP information, ping monitoring, per-process connections and diagnostics, all in one modern dashboard.

**Platform:** Windows 10/11

---

## ✨ Features

- 📊 **Live dashboard:** real-time download/upload speed, live chart, and total usage (system + this app)
- 🖧 **Network adapters:** status, type, link speed, IPs, active-adapter selection + DNS manager
- 🌐 **IP information:** local IPv4/IPv6 + public IP with country / city / ISP / timezone
- 📶 **Ping monitor:** custom targets + searchable list of well-known DNS / websites; live min/max/avg and packet loss
- ⚙️ **Per-process connections:** full TCP/UDP socket list for every app; click any IP for a live probe (ping, port check, reverse DNS, geo)
- 🚀 **Speed test:** real download / upload / latency (Cloudflare)
- 🛡️ **VPN detection** and smart alerts + **event history**
- 🖥️ **System tray:** close-to-tray, low background usage
- 🔄 **In-app updates:** notified inside the app when a new release is published; update with one click
- 🔒 **Offline-first:** the core works without internet (only public IP, geo and speed test are optional online features)

---

## 🚀 Installation & usage (for users)

1. Download the **latest release** from the [Releases page](https://github.com/X314S/netwatch/releases) and extract the zip — you'll get a `NetWatch` folder (put it anywhere, e.g. `C:\NetWatch`).
2. Run **`NetWatch.exe`** inside it. That's it — no Python or Node required.

> **WebView2:** the UI uses the Windows WebView2 runtime, which ships with Windows 10/11 in most cases. If it's missing, the app runs the bundled installer automatically (inside the `redist` folder).

### First run
- The window opens and NetWatch also lives in the **system tray** (near the clock).
- Closing the window hides it to the tray (monitoring continues). To fully quit: right-click the tray icon → **Exit**.

---

## 🖥️ Using the app

| Section | What it does |
|---------|--------------|
| **Dashboard** | Overview: speed, IP, ping |
| **Network** | Adapters, DNS, per-process connections, speed test |
| **Ping** | Ping monitor + famous DNS/website presets (search & add) |
| **History** | Event log (connect/disconnect, alerts, …) with filters |
| **Diagnostics** | Full network report + Copy button |
| **Settings** | Theme & accent color, update interval, ping threshold, launch on startup, clear history, reset preferences, check for updates |

### Updates
- The app checks GitHub for new releases on startup and via the **Check** button in Settings.
- When a newer version exists, an **"Update vX"** button appears in the top bar → download and **Install & Restart**.

---

## 📄 License

NetWatch is **proprietary software** — all rights reserved. See [LICENSE](LICENSE).
