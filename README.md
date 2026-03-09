# Jukebox

Interactive retro jukebox built with a single HTML file, custom PNG skins, and vanilla JavaScript audio controls.

## Features

- Clickable genre buttons on top of the jukebox art
- Genre-based jukebox skin switching (same layout, different style)
- Play/Pause transport control
- Animated status and now-playing text effects
- Responsive retro animated page background

## Project Files

- `index.html` - main entry point (recommended for GitHub Pages)
- `jukebox (1).html` - working source copy used during editing
- `jukebox.png` - default Pop skin
- `acoustic.png`, `trap.png`, `drill.png`, `punk.png` - alternate skins

## Genre to Skin Mapping

- `Pop` -> `jukebox.png`
- `Acoustic` -> `acoustic.png`
- `Trap` -> `trap.png`
- `Drill` -> `drill.png`
- `Punk` -> `punk.png`

## Audio Library

Current tracks are loaded from the `audio/` folder in `index.html`:

- `audio/pop1.mp3`
- `audio/hiphop1.mp3`
- `audio/edm1.mp3`
- `audio/rock1.mp3`
- `audio/jazz1.mp3`
- `audio/disco1.mp3`

If a file is missing, the related button can still switch skin but audio will not play for that track.

## Run Locally

From the project folder:

```bash
python3 -m http.server 8000
```

Then open:

`http://localhost:8000/index.html`

## Deploy on GitHub Pages

1. Push this folder to the `main` branch of your GitHub repo.
2. In GitHub: **Settings -> Pages**.
3. Under **Build and deployment**, choose:
   - **Source:** Deploy from a branch
   - **Branch:** `main` / `/ (root)`
4. Save and wait for the Pages URL to appear.

### Live Play Link

Use this direct link to open and play the jukebox:

- [https://wearenextgen.github.io/Jukebox/](https://wearenextgen.github.io/Jukebox/)

### Embed Link (iframe)

You can embed the jukebox on another page with a responsive wrapper:

```html
<div style="position:relative;width:100%;height:min(90vh,900px);">
  <iframe
    src="https://wearenextgen.github.io/Jukebox/?embed=1"
    title="Jukebox"
    style="position:absolute;inset:0;width:100%;height:100%;border:0;background:transparent;"
    allow="autoplay"
    loading="lazy"
  ></iframe>
</div>
```

## Notes

- Skin files should be true PNGs with alpha if you want transparent outer areas.
- For browser cache issues, hard refresh after replacing image files.
