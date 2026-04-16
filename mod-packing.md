### Mod structure

Every mod must be a **folder** containing at minimum a `mod.json` file.
The manager will silently ignore any folder that does not have one.

```
YourModFolderName/
├── mod.json          ← required
├── preview.png       ← optional, shown as the tile cover image (max 256×256 px)
└── ... your mod files (WRAP archives > textures, ent, mesh, askl, mat, etc.); example: MEGACITY > _F029.0xEE185533.MEGACITY.pcapk > 0x8C78CAA6.spiderlogo000.wrap.mesh
```

The folder name becomes the key written to `mods.config.ini` — keep it unique, use underscores instead of spaces.

### mod.json reference

```json
{
    "name":    "Your Mod Name",
    "version": "1.0",
    "author":  "Your Nickname",
    "image":   "image.png"
}
```

| Field | Required | Description |
|---|---|---|
| `name` | **Yes** | Display name shown in the mod tile |
| `version` | No | Version string, e.g. `"1.0.0"` or `"beta"` |
| `author` | No | Your name or handle |
| `image` | No | Filename of the preview image, relative to the mod folder |

> `name` is the only mandatory field. If it is missing or empty the mod will not be recognised by the manager.

### Preview image

- Formats: PNG, JPG, BMP
- Maximum size: **256×256 px** — larger images are automatically downscaled and centre-cropped
- Recommended: square images at exactly 256×256 px for the sharpest result

### Packaging as a .zip archive

Zip the **mod folder itself**, not its contents:

```
Correct — the folder is inside the archive:
MyAwesomeMod.zip
└── MyAwesomeMod/
    ├── mod.json
    ├── preview.png
    └── WRAP Directories

❌ Wrong — files are loose at the archive root:
MyAwesomeMod.zip
├── mod.json
├── preview.png
└── WRAP Directories
```

The name of the `.zip` file does not matter — the manager uses the **folder name inside the archive** as the mod identifier.

### mods.config.ini format

The config file is managed automatically. Its format is plain key=value:

```ini
MyAwesomeMod=1
AnotherMod=0
ThirdMod=1
```

`1` = enabled, `0` = disabled. Entries are added on install, updated on toggle, and removed on delete. The rest of the file is never touched.

### Complete example

A mod called **Red Dark Theme Concept** by **Kelthic**, version **1.0.0**:

**Folder layout:**
```
Red_Dark_Theme_Concept/
├── mod.json
├── preview.png
└── WRAP Directories
```

**mod.json:**
```json
{
    "name":    "Red Dark Theme Concept",
    "version": "1.0.0",
    "author":  "Kelthic",
    "image":   "preview.png"
}
```

Pack into `Red_Dark_Theme_Concept.zip` containing the folder above, share the zip, done.

---

## License

This project is provided as-is for the Spider-Man: Web of Shadows modding community.
