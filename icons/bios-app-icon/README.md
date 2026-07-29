# BIOS app icon (favicon / app tile)

The canonical BIOS shield mark (hexagon outline + wave) used as the favicon and
app icon across every BIOS web property (thebios.app and all `*.thebios.app`
MCP servers). Master lives in the vault at
`Resources/brand/bios/top-level/BIOS-Top-Level-Shield-Icon-Package`; this folder
is the public CDN mirror.

Reference colors: navy mark `#010E23`, dark-mode background `#091124`, slate wave
and lower shield `#607DA3`, white `#FFFFFF`.

## Files

- `bios-shield-icon-1024.png` — master mark, transparent, 1024x1024.
- `bios-shield-icon-512.png` / `-128.png` / `-32.png` — light-default app-icon
  sizes (navy + slate mark on light/transparent), matching the live favicon.
- `favicon-light.*`, `favicon-light.svg` — the light default favicons
  (white background, navy mark) used across the thebios.app properties.
- `favicon.ico`, `favicon-16/32/48x32.png`, `favicon.svg` — dark alternate
  (navy rounded square) for dark-only surfaces.
- `apple-touch-icon.png` (+ `-light`), `android-chrome-192/512`, `maskable-icon-512`,
  `safari-pinned-tab.svg`, `site.webmanifest` — full PWA / mobile set.

Served via `https://raw.githubusercontent.com/BW-BIOS/bhg-brand-assets/main/icons/bios-app-icon/<file>`.

Light is the standard: the thebios.app home/login and all `*.thebios.app`
surfaces render light, so the live favicon is the light (navy-on-light) mark.
Use the dark (navy-square) files only for dark-only surfaces. Do not recolor;
regenerate from the vault master.
