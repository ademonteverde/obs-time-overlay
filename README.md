# obs-time-overlay
A customizable clock overlay for OBS Studio with a settings control dock.

✅ Live-updating clock  
✅ Change font, size, color, and timezone  
✅ Settings sync in real-time between Dock and Clock display  
✅ Easy to load into OBS as a browser source  

---

## Files

- clock.html - The clock overlay to display in OBS Studio
- dock.html - The settings dock to control the clock overlay on OBS Studio

---

## Usage

### 1. Setup

1. Clone or download this repository to your computer.
2. Open OBS Studio and create a new scene if needed.
3. To add the Clock Overlay to the scene:
    - Add a new **Browser Source** to the scene.
    - Tick the **Local file** checkbox.
    - Set the **URL** to the `clock.html` file in the repository.
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

- Change **Clock color**
- Change **Clock font** and **Font size**
- Select **timezone**

---

## How It Works

- The Settings Dock (`dock.html`) sends settings to the Clock Overlay (`clock.html`) using:
    - `localStorage` (for persistence)
    - `BroadcastChannel` (for instant sync while OBS is running)
- The clock auto-updates every second.
- You can adjust font, size, color, timezone in real-time without restarting OBS.

---

## Notes 

- Tested with OBS 30+
- **OBS Browser Source** sometimes blocks `file:///` — using `http://absolute/` works reliably
- **BroadcastChannel** is used for fast settings sync 

## Future Ideas

- Option to toggle **time format** (12h / 24h)
- Option to toggle **seconds**
- Option to **include date**
- Custom **font upload**
- Preset themes/ styles

---

## License
MIT License

Copyright (c) 2025 Andre Carlo Demonteverde