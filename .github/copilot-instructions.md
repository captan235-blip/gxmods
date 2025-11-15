# Copilot Instructions for GX Mods Repository

## Overview
This repository contains GX Mods, a collection of customizations for the Opera GX browser. Mods can modify the browser's appearance, sounds, music, themes, wallpapers, and web content using shaders and CSS. The repository is structured to facilitate the creation, testing, and sharing of mods.

## Repository Structure
- **`mods/`**: Contains individual mods, each in its own folder. Key components include:
  - `manifest.json`: Defines the mod's metadata and configuration.
  - Subfolders like `music/`, `shaders/`, `css/`, `sounds/`, and `wallpaper/` for specific mod assets.
- **`documentation/`**: Contains guidelines and references for creating mods.
  - `guidelines.md`: Best practices for optimizing resources, shaders, sounds, and themes.
  - `mods.md`: Detailed documentation on modding capabilities.
  - `shaders.md`: Specific rules and examples for writing shaders.
- **`tools/livepreview/`**: Scripts and resources for previewing mods locally.
  - `livepreview.py`: A Python script for testing shaders and other mod components.

## Key Development Workflows
### Creating a New Mod
1. Use the `Mod_Template` directory in `documentation/` as a starting point.
2. Populate `manifest.json` with metadata.
3. Add assets to appropriate subfolders (e.g., `music/`, `shaders/`).
4. Follow the guidelines in `documentation/guidelines.md` to ensure quality.

### Testing Mods Locally
1. Open Opera GX and navigate to `opera:extensions`.
2. Enable Developer Mode.
3. Click `Load unpacked` and select the mod's directory.
4. Test the mod in the browser.

### Sharing Mods
1. Navigate to `opera:extensions`.
2. Enable Developer Mode.
3. Click `Pack extension` and select the mod's directory.
4. Upload the resulting `.CRX` file to [GX.store](https://operagx.gg/mods2) via [GX.create](https://create.gx.games/mods).

## Project-Specific Conventions
- **Shaders**:
  - Write shaders in SkSL (Skia Shading Language).
  - Optimize for performance; avoid unnecessary uniforms and high frame rates.
  - Include both animated and static versions if possible.
- **Sounds**:
  - Use MP3 format for browser sounds and WAV for keyboard sounds.
  - Ensure sounds are short, responsive, and free of initial silence.
- **Themes**:
  - Provide both light and dark versions.
  - Use the built-in color picker for consistent results.
- **Wallpapers**:
  - Follow the `GXWallpaperGuidelines.pdf` for composition and resolution.
  - Use JPG for static wallpapers and VP9 for animated ones.

## Integration Points
- **GX.store**: Mods are uploaded and shared via [GX.store](https://operagx.gg/mods2).
- **Live Preview**: Use the `tools/livepreview/` scripts to test shaders and other assets locally.

## Examples
- Refer to `mods/Cozy/` for a mod with shaders, sounds, and themes.
- Check `mods/Discord_Amoled/` for CSS-based web modding.
- See `mods/Full_Weather_Cycle/` for an animated shader example.

## External Dependencies
- Python: Required for running `tools/livepreview/livepreview.py`.
- Opera GX: Necessary for testing and deploying mods.

## Notes
- Always credit third-party resources and include licenses where applicable.
- Optimize assets to minimize mod size and improve performance.

For more details, refer to the [README.md](../README.md) and [documentation/](../documentation/) folder.