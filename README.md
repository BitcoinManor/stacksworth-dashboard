# ⚡ STACKSWORTH DASHBOARD  
**Open Source • Web Flashable • Bitcoin Metrics Display • Bitcoin at a Glance**

![STACKSWORTH Banner](https://github.com/BitcoinManor/STACKSWORTH_Matrix/raw/main/assets/stacksworth_banner.png)

Welcome to **STACKSWORTH**, the future of open-source Bitcoin displays.  

**This is Bitcoin’s Pulse, at a glance.**
is a project that stems from Blokdbit that turned into STACKSWORTH with the Matrix and Pulse as the two flagship models. This dashboard Displays the metrics that you will find on all our Stacksworth Models.
Please let us know what you think 
**Bitcoin’s Pulse at a Glance — a neon, LVGL-style web dashboard.**

Born on **Matrix**, forged in **Spark (7")**, creating a **Pulse (5")**, pushing to the **Edge (7")**, and reaching **Infinity (10")**. This project mirrors our firmware UI with a cyberpunk feel: **price**, **block height**, **mempool & fee tiers**, and **miner tags** — at a glance.

---

## Why this exists
Not everyone can (or wants to) buy the hardware. This is the **public, browser-based version** of what our devices show — the same vibe, same layout philosophy, same “at-a-glance” focus.

- ⚡ **Fast to load** — single HTML file, no build step required  
- 🧠 **LVGL-inspired UI** — arcs, gauges, sparklines, interval bars  
- 🧩 **Shareable components** — style tokens we can mirror in firmware  
- 🖥️ **Kiosk-friendly** — perfect for a Raspberry Pi on a wall display

---

## What’s inside (v1 HTML mock)
- `stacksworth_timechain_dashboard.html` — a single page with:
  - **BTC price** (USD, CAD est.), **24h sparkline + range**
  - **Latest block** number, **age**, **miner name** 
  - **Mempool** backlog, **fee tiers** (low/med/high), **capacity arc**
  - **Block Interval Visualizer** (10-minute target line)
  - **Theme toggle**, **responsive grid**, and mock data you can swap for APIs

> Live data wiring comes next using our very own API's
> like these ones and more
>  SATONAK API'S
- - [`Satonak Price`](https://www.satonak.bitcoinmanor.com/api/price)
  - - - [`Satonak Block Height`](https://www.satonak.bitcoinmanor.com/api/height)
     
    - TH Matrix  
**Open Source • Web Flashable • Bitcoin at a Glance**

![STACKSWORTH Banner](https://github.com/BitcoinManor/STACKSWORTH_Matrix/raw/main/assets/stacksworth_banner.png)

Welcome to **STACKSWORTH**, the future of open-source Bitcoin displays.  
Watch Bitcoin's Pulse at a Glance in real time  — price, block height, mempool fees, sats/dollar and weather — all from a sleek, plug-and-play LED matrix 
that’s built for Bitcoiners, by Bitcoiners.

---

## 🚀 Latest Firmware: v1.0.2

🆕 MAC-based AP ID (e.g. `SW-MATRIX-E4E204`)  
🌐 Matching ID in hotspot, HTML portal, and network list  
🛠️ Improved UX for multi-device setups and flashing

📦 [Download v1.0.2 ZIP](https://github.com/BitcoinManor/STACKSWORTH_MATRIX/releases/download/v1.0.2/STACKSWORTH_MATRIX_v1.0.2.zip)  
📓 [See Changelog](https://github.com/BitcoinManor/STACKSWORTH_MATRIX/blob/main/CHANGELOG.md)

---

## 🚀 Quick Start

- **🔌 Flash Instantly:**  
  [StacksWorth Web Flasher →](https://bitcoinmanor.github.io/STACKSWORTH_WebFlasher) *(custom URL coming soon)*

- **📦 Order Units or Kits:**  
  [stacksworth.com](https://stacksworth.com),
  [Bitcoin Manor](https://BitcoinManor.com)
  

- **🛠 Full Source Code + Firmware:**  
  [STACKSWORTH GitHub](https://github.com/BitcoinManor/STACKSWORTH_Matrix)

-🧡 Stacksworth & Bitcoin Manor
This project is part of the STACKSWORTH ecosystem — handcrafted Bitcoin displays engineered for your home, workspace, studio, or node room.

Follow the journey:

❌ [X / Twitter:](https://x.com/stacksworth)
X-[BitcoinManor](https://x.com/BitcoinManor)
📸 [Instagram:](https://instagram.com/bitcoinmanor)
🌐 Website: [STACKSWORTH:](//stacksworth.com)
🌐 [Bitcoin Manor:]( https://bitcoinmanor.com)

---

## 💡 What Is STACKSWORTH Matrix?

The **STACKSWORTH Matrix** is a self-contained, open-source Bitcoin display system featuring:

- 🧠 Real-time Bitcoin metrics
- 🔥 Dual-row LED scrolling text
- 🌐 Easy AP-mode configuration (WiFi, city, timezone)
- 💻 Full Arduino-based firmware for developers
- 🟩 Web flashable from any modern browser

Built for signal, not noise.

---

## 🧱 Metrics Displayed

- **💰 BTC Price (USD)** — via CoinGecko  
- **📦 Block Height** — via Blockchain.info  
- **🚦 Fee Rate (sat/vB)** — via Mempool.space  
- **🌤 Local Weather + Temp** — via OpenWeatherMap  
- **⏰ Time** — via NTP

Future versions will include:
- 🏷️ Miner Tag Detection  
- 📶 MAC ID–based SSID Broadcasting  
- 🎲 Weighted Animation Mode (Smash Buy Button)

---

## 🛠 Tech Stack

- **Hardware:** ESP32 (NodeMCU or similar), 64x16 LED matrix
- **Firmware:** Arduino/C++  
- **Web Config:** SPIFFS + AsyncWebServer  
- **APIs:**
- We use our own SatoNak Server and thank the others below that we use for our backups
- SATONAK API'S
  - - - [`Satonak Price`](https://www.satonak.bitcoinmanor.com/api/price)
  - - - [`Satonak Block Height`](https://www.satonak.bitcoinmanor.com/api/height)
  - - - [`Satonak CAD Price`](https://satonak.bitcoinmanor.com/api/price?fiat=CAD)
  - - - [`Satonak Fee`](https://satonak.bitcoinmanor.com/api/fee)
  - - - [`Satonak Hashrate`](https://satonak.bitcoinmanor.com/api/hashrate)
  - - - [`Satonak Circulating Supply`](https://satonak.bitcoinmanor.com/api/circsupply)
  - - - [`Satonak Miner`](https://satonak.bitcoinmanor.com/api/miner)
  - - - [`Satonak 24hr Price Chamge`](https://satonak.bitcoinmanor.com/api/change24h)
  - - - [`Satonak EUR Price`](https://satonak.bitcoinmanor.com/api/price?fiat=EUR)
        OTHER BACKUP
      -
      - The HTML already includes stable element IDs and comments so integration is simple.

---

## Live demo
👉 (https://bitcoinmanor.github.io/stacksworth-dashboard/)

1. click the link above and it will open it in your browser.  
2. Click **Refresh** (simulates new data)  **Accent** (switches accent color) **Mode** (changes light to dark mode)

> For real API calls from a local file, you may need to serve it over `http://` to avoid CORS surprises. Use any static server (examples below).

---

## Wire it up (next step)
Suggested data sources:We use our own SatoNak Server and thank the others below that we use for our backups
- **Price + 24h chart**: CoinGecko  
  - `/api/v3/simple/price?ids=bitcoin&vs_currencies=usd,cad&include_24hr_change=true`  
  - `/api/v3/coins/bitcoin/market_chart?vs_currency=usd&days=1`
- **Fees + mempool**: mempool.space  
  - `/api/v1/fees/recommended`, `/api/mempool`  
- **Latest block + miner tag**: mempool.space  
  - `/api/blocks` then `/api/block/{hash}/txs/0` (coinbase decode → pool name)

> Tip: If your browser blocks cross-origin calls, run a tiny local proxy or host this page on a small server (see **Local dev**).

---

## Device lineup (shared design language)
We keep one **visual grammar** across web and devices.

- **Pulse (5")** — compact layout, larger touch targets  
- **Edge (7")** — current reference layout (great density)  
- **Infinity (10")** — more columns and richer charts  
- **Matrix** — LED models that started the “Pulse at a Glance” journey  
- **Spark (7")** — ESP32-S3 + LVGL, our firmware twin of this dashboard

**Coming soon:** device presets via URL, e.g.  
`?device=pulse | edge | infinity` → auto scales fonts, paddings, and chart heights.

---

## Local dev
Pick one:

**Python (built-in)**
```bash
# from the repo root
python3 -m http.server 8000
# open: http://localhost:8000/stacksworth_timechain_dashboard.html
```

**Node (serve)**
```bash
npm i -g serve
serve .
```

**VS Code Live Server**  
Right-click the HTML → **Open with Live Server**.

---

## Raspberry Pi kiosk (mini guide)
- Raspberry Pi OS, enable boot to desktop
- Auto-launch Chromium in kiosk mode (example command):
```bash
chromium-browser --kiosk --incognito --noerrdialogs \
  --check-for-update-interval=31536000 \
  file:///home/pi/stacksworth-dashboard/stacksworth_timechain_dashboard.html
```
- Optional: host from a tiny Flask/Node service and point the Pi at `http://<pi-ip>/dashboard`.

---

## Roadmap
- [ ] Wire live data (CoinGecko + mempool.space)  
- [ ] Miner decode: coinbase tag → pool map (fallback “Unknown”)  
- [ ] Device presets (`?device=pulse|edge|infinity`)  
- [ ] Small server proxy (optional) to smooth CORS/rate limits  
- [ ] Add screenshots & branding assets  
- [ ] Publish a minimal theme guide for LVGL ↔︎ Web parity  
- [ ] GitHub Pages demo

---


## ⚡ SatoNak API's  ⚡

- SATONAK API'S
  - - - [`Satonak Price`](https://www.satonak.bitcoinmanor.com/api/price)
  - - - [`Satonak Block Height`](https://www.satonak.bitcoinmanor.com/api/height)
  - - - [`Satonak CAD Price`](https://satonak.bitcoinmanor.com/api/price?fiat=CAD)
  - - - [`Satonak Fee`](https://satonak.bitcoinmanor.com/api/fee)
  - - - [`Satonak Hashrate`](https://satonak.bitcoinmanor.com/api/hashrate)
  - - - [`Satonak Circulating Supply`](https://satonak.bitcoinmanor.com/api/circsupply)
  - - - [`Satonak Miner`](https://satonak.bitcoinmanor.com/api/miner)
  - - - [`Satonak 24hr Price Chamge`](https://satonak.bitcoinmanor.com/api/change24h)
  - - - [`Satonak EUR Price`](https://satonak.bitcoinmanor.com/api/price?fiat=EUR)
     
---        

## Contributing
PRs welcome! Keep changes small and testable. If you’re adding APIs or presets, include a short note and a screenshot/gif.

---

## License
MIT

---

## Credits
- **StacksWorth** — Bitcoin’s **Pulse at a Glance**  
- Thanks to the open data community behind **CoinGecko** and **mempool.space**.

---

## Screenshots
_Adding images here once we’re wired live data and finalized the color tokens._  
`/assets/screenshot-01.png`  
`/assets/screenshot-02.png`

---

### Notes for firmware parity
We’ll mirror the CSS tokens (colors, radii, borders) into LVGL styles so Spark/Edge/Pulse/Infinity feel identical to the web dashboard. That way, design work happens once and ships everywhere.
