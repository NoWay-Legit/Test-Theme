Performance & Preprocessing Notes
================================

This project includes PostCSS-based preprocessing to support splitting source files
and producing a minified single-file theme for BetterDiscord / Vencord.

Key recommendations implemented or to follow:

- Use PostCSS + postcss-easy-import to split CSS into logical files under /src.
- Use `npm run build` (dev) and `npm run build-prod` (production/minified).
- Avoid deep descendant selectors like `.a .b .c` — prefer class repetition or closer ancestors.
- Avoid attribute partial-match selectors (`[attr*=val]`) when possible.
- Limit animations and prefer `transform` and `opacity` for GPU-accelerated changes.
- Add `will-change` for elements that will animate (sparingly): e.g. `.button-38aScr { will-change: transform; }`
- Respect `prefers-reduced-motion` (already implemented).
- Place remote `@import` lines after the metadata header in the final .theme.css file so BetterDiscord will accept them.

Sources: BetterDiscord docs - Preprocessing, Performance, Remote Imports.
