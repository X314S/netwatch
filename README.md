# NetWatch

**NetWatch** is a lightweight, offline-first Windows desktop app for network monitoring — network adapters, live internet speed, IP information, ping monitoring, per-process connections, a network toolkit and diagnostics, all in one modern dashboard.

**Platform:** Windows 10/11

---

## ✨ Features

- 📊 **Live dashboard:** real-time download/upload speed, live chart, total usage (system + this app), public-IP geo card and top processes
- 🖧 **Network adapters:** status, type, link speed, IPs, active-adapter selection + DNS manager
- 🌐 **IP information:** local IPv4/IPv6 + public IP with country / city / ISP
- 📶 **Ping monitor:** custom targets + searchable presets of well-known DNS / websites; live min/max/avg and packet loss
- ⚙️ **Active Connections:** per-process TCP/UDP socket tables with protocol filter chips, live traffic dots, summary counters and an inline endpoint inspector (ping / location / port / rDNS)
- 🧰 **Network Toolkit:** DNS/ARP/Routing, Traceroute, Port / LAN / Wi‑Fi scanners, Whois, WOL, SSL checker, HTTP tester, hosts editor / DNS flush / network reset / firewall manager — with snapshots & undo
- 🚀 **Speed test:** real download / upload / latency from **Cloudflare, Fast.com or Ookla** — live phase feedback (Starting → Latency → Download → Upload), live Mbps, elapsed timer and a Cancel button
- 🖼️ **Mini-HUD overlay:** an always-on-top strip of live speed/ping/totals that docks to the top edge, can be pinned, works on your chosen monitors, adjusts opacity/click-through, and has a **Process Watch** panel
- 🛡️ **VPN detection**, smart alerts + **event history** and restore points
- 🖥️ **System tray:** close-to-tray, low background usage, global hotkeys (`Ctrl+Alt+N/H/L`)
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
| **Dashboard** | Overview: speed, IP, ping, top processes |
| **Network** | Adapters, DNS, Active Connections, speed test |
| **Tools** | Ping monitor, DNS/ARP/Routing, scanners, diagnostics tools |
| **History** | Event log (connect/disconnect, alerts, …) with filters |
| **Restore** | System snapshots & undo for destructive changes |
| **Settings** | Theme & accent color, update interval, ping threshold, notifications, launch on startup, mini-HUD, clear history, reset preferences, check for updates |

### Updates
- The app checks GitHub for new releases on startup and via the **Check** button in Settings.
- When a newer version exists, an **"Update vX"** button appears in the top bar → download and **Install & Restart**.

---

## 📄 License

NetWatch is **proprietary software** — all rights reserved. See [LICENSE](LICENSE).
