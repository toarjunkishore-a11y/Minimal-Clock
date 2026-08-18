# Minimal Clock

A minimal dot-matrix timer, stopwatch, and clock — inspired by Nothing's glyph/LED aesthetic. Every digit and letter is hand-drawn as a 5×7 dot grid in pure HTML/CSS/JS. No fonts, no libraries, no build step.

**[Live demo →](https://toarjunkishore-a11y.github.io/Minimal-Clock/)**

![screenshot placeholder](screenshot.png)

## Features

- **Timer** — editable hours / minutes / seconds with +/– steppers, start, pause, resume, reset
- **Stopwatch** — start, stop, lap tracking, reset
- **Clock** — live current time in dot-matrix, day/date readout, 12H / 24H toggle
- **Timer completion** — a smooth 3-note chime (synthesized live with the Web Audio API, no audio files), a flashing display, and a full-screen "TIME UP" notification with a DISMISS button. Also tries to fire a native OS notification if permission is granted.
- **Fullscreen button** — one tap puts the whole app into fullscreen, with the icon swapping to reflect state
- **Ambient mouse animation** — a soft spotlight follows the cursor and the display drifts with a subtle parallax
- Faint background grid + ghost dots for the authentic LED-matrix look
- Runs completely offline, single self-contained `index.html`
- Responsive down to mobile, respects `prefers-reduced-motion`

## Run locally

Just open `index.html` in any browser — that's it, no install needed.

```bash
git clone https://github.com/toarjunkishore-a11y/Minimal-Clock.git
cd Minimal-Clock
open index.html   # or double-click the file
```

## Deploy on GitHub Pages

1. Push this repo to GitHub.
2. Go to **Settings → Pages**.
3. Under **Source**, select the `main` branch and `/ (root)` folder.
4. Save — your app will be live at `https://toarjunkishore-a11y.github.io/Minimal-Clock/`.

## Tech

Plain HTML, CSS, and vanilla JavaScript.

- The dot-matrix "font" is a hand-built 5×7 bitmap glyph table rendered as CSS grid `div`s — fully hackable, add new characters or change dot size/spacing/color via the CSS variables at the top of the file.
- The end-of-timer chime is synthesized in-browser with the Web Audio API (three sine oscillators through a lowpass filter), so there's no audio asset to host.
- Fullscreen uses the standard `requestFullscreen` / `exitFullscreen` API with a WebKit fallback for Safari.

## License

MIT — do whatever you want with it.
