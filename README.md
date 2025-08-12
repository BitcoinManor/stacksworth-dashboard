# StacksWorth Dashboard  
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

> Live data wiring comes next (CoinGecko + mempool.space). The HTML already includes stable element IDs and comments so integration is simple.

---

## Live demo
👉 (https://bitcoinmanor.github.io/stacksworth-dashboard/)

1. click the link above and it will open it in your browser.  
2. Click **Refresh** (simulates new data)  **Accent** (switches accent color) **Mode** (changes light to dark mode)

> For real API calls from a local file, you may need to serve it over `http://` to avoid CORS surprises. Use any static server (examples below).

---

## Wire it up (next step)
Suggested data sources:
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
