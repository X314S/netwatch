<div align="center">

![Release](https://img.shields.io/github/v/release/X314S/netwatch?color=4FFF4D)
![Downloads](https://img.shields.io/github/downloads/X314S/netwatch/total?color=1E90FF)
![Platform](https://img.shields.io/badge/platform-Windows-0078D6)
![Status](https://img.shields.io/badge/status-active-4FFF4D)

</div>

# NetWatch

**[English](README.md)** · [فارسی](README.fa.md)

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

## ✅ Verifying downloads

Every release ships a `SHA256SUMS` file next to the zip. Before running anything, verify the archive you downloaded:

**Windows (PowerShell):**
```powershell
# compare the output with the hash listed in SHA256SUMS
certutil -hashfile NetWatch-portable-<version>.zip SHA256
```

**Windows / Linux / macOS (sha256sum):**
```bash
# download SHA256SUMS from the release and run:
sha256sum -c SHA256SUMS        # → "NetWatch-portable-<version>.zip: OK"
```

The app itself re-verifies this checksum before applying an in-app update — a mismatched archive is never applied.

---

## 🔒 Privacy

**What NetWatch does NOT do:** it has no account system, no API keys, and it does not collect or store any personal data. Everything the app displays — network adapters, traffic, per-process connections, DNS configuration, hosts file, history, restore points — is gathered through local Windows APIs and **stored only on your device** (in the app's local data folder). None of that data is ever transmitted anywhere.

**The complete list of outbound network requests** (nothing else leaves your device):

| Feature | Where it connects | What is sent |
|---|---|---|
| Public IP / geo card | `ip-api.com` (+ fallbacks `ipwho.is`, `ipapi.co`, `ipify`) | Your public IP address (inherent to the feature) |
| Update check | `api.github.com` (X314S/netwatch) | Nothing but the request itself |
| Ad banner | NetWatch Cloudflare Worker | Ad campaign ids; banner images |
| Anonymous daily ping | NetWatch Cloudflare Worker | A random anonymous install id + app version — nothing else (see below) |
| Speed test / Whois / SSL / HTTP tester / DNS tools | The servers you choose (Cloudflare, Fast.com, Ookla, RDAP, …) | Only what the tool you ran sends to the target you picked |

### Anonymous daily ping — in short

No data is sent. Once a day the app reports a random anonymous install id (generated on your device) + the app version, so the developer can count active installs. That's all — no name, no IP, no device or usage data.

---

## ⚠️ Disclaimer

NetWatch is a **network display and diagnostic tool**. It is provided **"AS IS", without warranty of any kind** — express or implied, including fitness for a particular purpose.

- You are solely responsible for how you use it. **Misuse of the toolkit (firewall changes, network reset, hosts-file edits, admin-level commands, or killing processes based on incomplete information) is entirely your responsibility** and may disrupt your system or network.
- The developer/team is **not liable** for any damage, data loss, or disruption resulting from the use — or misuse — of the software or its features.
- Always confirm before destructive actions; the app offers restore points for most system changes — use them.

---

## 📄 License

NetWatch is **proprietary software** — all rights reserved. See [LICENSE](LICENSE).
