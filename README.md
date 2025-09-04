# NebulaGlass (BetterDiscord/Vencord Theme)

A sleek glassmorphism theme for Discord with accessible contrast, reduced-motion support, and adjustable accent color.

## Features
- Single-file **`NebulaGlass.theme.css`** compatible with BetterDiscord and Vencord
- Adjustable variables (accent, blur, transparency, radii, fonts)
- Respects **prefers-reduced-motion**
- Light & Dark support
- Uses trusted remote imports (Google Fonts)

## Quick Start
1. Download the file from `dist/NebulaGlass.theme.css`.
2. Place it in your themes folder:
   - **Windows:** `%appdata%/BetterDiscord/themes`
   - **macOS:** `~/Library/Application Support/BetterDiscord/themes`
   - **Linux:** `~/.config/BetterDiscord/themes`
3. Enable it in BetterDiscord or Vencord.
4. To customize, edit `:root` variables via the theme editor.

## Development
- The BetterDiscord docs require themes to be **single-file CSS** named `*.theme.css`.
- This repo keeps readable sources in `/src` and ships a ready bundle in `/dist`.

### Build (optional)
If you want to regenerate the dist file from `/src`, you can use PostCSS + cssnano:
```bash
npm i -D postcss postcss-cli cssnano
npx postcss src/index.css -u cssnano -o dist/NebulaGlass.theme.css
```
*(Building is optional; the provided `dist/NebulaGlass.theme.css` is already ready.)*

## Guidelines
This project follows BetterDiscord’s theme guidelines: public repo, no harmful code, accessible design, and trusted remote imports.

## License
MIT
