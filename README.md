# exWoS Mod Manager

A modern minimal mod manager for **Spider-Man: Web of Shadows**.
Install, enable, disable, and remove mods without touching any config files manually.

Based on Kirbystealer [exWoS Mod Framework](https://github.com/kirbystealer/WebOfShadowsTools/releases). Actual version at this moment: `0.0.3 alpha`

---

## For Users

### Requirements

- Windows 7 / 8 / 10 / 11
- Spider-Man: Web of Shadows (PC)

### Installation

1. Download the latest **`exWoS Mod Manager.exe`** from the Releases or NexusMods
2. Place it anywhere you like but **NOT** in disk C. For example: `D:\Programs\WoSModManager
3. Launch it

### Setting up the game path

On first launch, point the manager to your game:

1. Click **Browse** and select `Spider-Man Web of Shadows.exe`, or paste the path directly into the field
2. Click **Apply** — the status pill in the top-right corner will turn green and show **Game found**

The path is saved automatically and remembered on every mod manager launch.

### Installing a mod

Mods are distributed as `.zip` archives. To install one:

- **Drag and drop** the `.zip` file onto the drop zone, or
- Click **or choose a file** and pick the archive from the file dialog

The mod will be extracted, validated, and appear in the **Installed mods** grid immediately.

> If the archive does not contain a valid `mod.json` file the mod will be rejected and not installed. Contact the mod author if this happens.

### Enabling and disabling mods

Each mod tile has a **toggle switch** in the bottom-left corner:

- **On** (blue) — the mod is active and will be loaded by the game
- **Off** (grey & dimmed) — the mod is present on disk but will be ignored by the game

Changes take effect the next time you launch the game.

### Removing a mod

Click the cross button on a mod tile. You will be asked to confirm — the mod folder will be permanently deleted from disk and its entry removed from the config.

### Language

Click **EN** or **RU** in the top-right header to switch the interface language. The preference is saved automatically.
