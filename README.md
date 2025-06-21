# 🕒 OBS Clock & Date Dock – v1.0.0
A customizable clock and date overlay system for OBS Studio with a visual control dock.

✅ Live-updating Clock and Date
✅ Control font, size, color, weight, timezone, and format
✅ Real-time settings sync between Dock and Displays
✅ Google Fonts support with live previews
✅ LocalStorage-based persistence
✅ Easy OBS integration as a browser source
✅ Clean, dark-themed UI inspired by OBS Yami Dock aesthetic

---

## Files

- `clock.html` – Clock overlay for OBS Studio

- `date.html` – Date overlay for OBS Studio

- `dock.html` – Settings dock to control both clock and date

---

## Usage

### 1. Setup

1. Clone or download this repository to your computer.
2. Open OBS Studio and create a new scene if needed.
3. To add the Clock or Date Overlay to the scene:
    - Add a new **Browser Source** to the scene.
    - Tick the **Local file** checkbox.
    - Set the **URL** to the `clock.html` or `date.html` file in the repository.
    - Click **OK**.
4. To add the Settings Dock to OBS Studio:
    - Go to **Docks** → **Custom Browser Docks**.
    - Set **Name** to: `OBS Clock Settings`.
    - Set **URL** to:  
      `http://absolute/` + the path to your `dock.html` file.  
      Example:  
      `http://absolute/C:/Users/dock.html`
    - Click **Apply**.

---

## Features

- ⏰ Clock customization

    - Font family (Google Fonts supported)

    - Font size and weight

    - Text color

    - Timezone selection

- 📅 Date customization

    - Multiple date formats (MM/DD/YYYY, dddd, MMMM D, YYYY, etc.)

    - Optional custom font, color, size

    - Toggle to match clock styling

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

- Tested with OBS 30+
- **OBS Browser Source** sometimes blocks `file:///` — using `http://absolute/` works reliably
- **BroadcastChannel** is used for fast settings sync 
- Settings persist across sessions — reset button restores to:
- Clock: black, sans-serif, 100px, normal
- Date: black, sans-serif, 40px, `MMMM D, YYYY`, local timezone

## Future Ideas

- ✅ Option to display **Date** *(now live!)*
- Option to display **Am/Pm**
- Option to toggle **time format** (12h / 24h)
- Option to toggle **seconds**
- Option to **include date**
- Custom **font upload**
- Preset **style themes**
- Sync between multiple clock overlays
- Export/import config

---

## License
MIT License

Copyright (c) 2025 Andre Carlo Demonteverde