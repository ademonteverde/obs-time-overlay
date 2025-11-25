# 🕒 OBS Clock & Date Dock
### Fully Customizable Clock + Date Overlays for OBS Studio

![version](https://img.shields.io/badge/version-1.0.0-blue)
![license](https://img.shields.io/badge/License-MIT-green.svg)
![html](https://img.shields.io/badge/HTML-5-orange.svg)
![obs](https://img.shields.io/badge/OBS-Compatible-302e31.svg)
![made-by](https://img.shields.io/badge/Made%20by-Andre%20Carlo%20Demonteverde-9cf)

A customizable clock and date overlay system for OBS Studio with a visual control dock.

✔ Live-updating clock and date  
✔ Google Fonts support  
✔ Real-time sync between dock + overlays  
✔ LocalStorage persistence  
✔ Clean, dark UI  
✔ Easy to install and control  

---

## Files

| File | Description |
|------|-------------|
| **clock.html** | Clock overlay for OBS |
| **date.html**  | Date overlay for OBS |
| **dock.html**  | Settings panel that controls both clock and date |

---

## Usage

### 1. Setup


### 1️⃣ Add the Clock or Date Overlay  
1. Open **OBS Studio**  
2. Add **Browser Source** → *Local File*  
3. Point it to `clock.html` or `date.html`  
4. Set the size (e.g., **800 × 300**)  
5. Done — overlay updates automatically

---

### 2️⃣ Add the Settings Dock  
1. Go to **Docks → Custom Browser Docks**  
2. Name: **OBS Clock Settings**  
3. URL format (required by OBS): 
    http://absolute/C:/path/to/dock.html
4. Click **Apply**  
5. The dock will appear and instantly control both overlays

---

## Features

- ⏰ Clock customization
    - 12-hour or 24-hour time  
    - Show or hide seconds  
    - Google Fonts support  
    - Font size & weight  
    - Text color  
    - Timezone selection  

- 📅 Date customization
    - Multiple date formats  
    - Optional custom font + size + color  
    - Match clock styling toggle  
    - Timezone-aware rendering  

- 🧠 Live sync & persistence
    - Instant updates via BroadcastChannel  
    - Settings saved using localStorage  
    - Reset button to restore defaults  

---

## How It Works

- `dock.html` controls both `clock.html` and `date.html`
- Uses `localStorage` to save settings between OBS sessions
- Uses `BroadcastChannel` to instantly sync changes while OBS is running
- Fonts are loaded dynamically from Google Fonts API based on input
- The clock auto-updates every second.
- You can adjust font, size, color, timezone in real-time without restarting OBS.

---

## Notes 

- Tested on **OBS 30+**  
- If OBS blocks `file:///`, use `http://absolute/`  
- Default reset values:  
- **Clock:** black, sans-serif, 100px  
- **Date:** black, sans-serif, 40px, `MMMM D, YYYY`

## Future Ideas

- Custom **font upload**
- Preset **style themes**
- Toggle AM/PM label  
- Sync between multiple clock overlays
- Export/import config

---

## License
MIT License
Copyright (c) 2025 Andre Carlo Demonteverde