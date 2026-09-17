# WiZ Home 💡

A minimal, no-cloud controller for WiZ smart bulbs. It talks directly to your
bulbs over UDP on your local network (port `38899`) — no account, no cloud,
no third-party app required. The interface is a small HTML app styled after
Apple Home, served locally and opened in a borderless browser window, so it
looks and feels the same on Windows, macOS, and Linux.

## ✨ Features
- **Full control:** on/off, brightness (10–100%), color temperature (2000K–6800K)
- **RGB color:** for bulbs that support it (detected automatically by model)
- **20 built-in scenes:** Cozy, Ocean, Sunset, Romance, Party, Forest, Relax,
  Focus, Wake up, Sleep, Night light, Candlelight, Movie, Club, and more
- **Auto-discovery:** finds every WiZ bulb on your Wi-Fi network automatically
- **Manual add:** add a bulb by IP if discovery misses it
- **Rename / remove** bulbs from the list
- **Zero external dependencies** — pure Python standard library, nothing to `pip install`
- **Cross-platform:** same codebase runs on Windows, macOS, and Linux

## 🛠️ Requirements
- Python 3.8+ (only needed if running from source — the prebuilt executables
  below don't need Python installed)
- A modern browser (Chrome, Edge, Chromium, or Brave give the cleanest
  "app-like" window; any other browser works as a fallback tab)
- WiZ bulbs connected to the same Wi-Fi network as the computer running this

## 🚀 Usage

### Prebuilt executable (no Python needed)
Download the file for your OS and run it directly:

| OS | File |
|---|---|
| Windows | `LuminaWizController.exe` |
| macOS | `LuminaWizController.app` (unsigned — see note below) |
| Linux | `LuminaWizController_Linux_x86-64` (run `chmod +x wiz_home` once) |

## 📝 Notes
- Paired bulbs are saved to `~/.wiz_home.json`.
- The macOS build isn't signed or notarized: the first time you open it,
  right-click → **Open** → **Open Anyway** to bypass Gatekeeper's warning.
- Tested against WiZ firmware 1.38.0 on E27 bulbs; other WiZ models using the
  standard UDP protocol should also work.

## 🗺️ Roadmap
- Signed/notarized installers
- Optional in-app language switch (English/Spanish)
