# HOFFMAN // EYE

A cyberpunk concept site about human and AI integration: the screen as an extension of
your eyes. One self-contained `index.html` of 27 kB, no build step, no framework, no
backend.

**[Live demo](https://hoffman-alternative.github.io/hoffman-eye/)**

## What it does

- Three parallax depth layers that tilt with the mouse, or with the gyroscope on phones.
- Navigation through the faces of a pyramid "eye"; each face is a section of the dossier.
- A photo you pick is processed in a canvas (glitch, RGB shift, noise, torn bytes,
  scanlines). It never leaves the browser: the page makes no network requests besides
  loading fonts.
- The palette follows the local time of day, from cool morning blue to a red night.
- Live HUD, terminal fonts, CRT effects, and a portrait mobile layout with chat-style tabs.

## Design decisions

- Single file on purpose. The site is a showcase that should open from disk, from GitHub
  Pages or from any static host without a toolchain. The cost is a long `index.html`
  that is harder to navigate than modules.
- No framework. DOM updates are a handful of `textContent` and template writes; a
  virtual DOM would add weight without removing code.
- User-entered text is HTML-escaped before it is rendered into the dossier card.

## Limits

- Fonts load from Google Fonts. Self-hosting them would remove the only third-party
  request.
- This repository holds the original concept version. The production site has since
  moved to a view-only layout and is not published here.

## Case studies

- [Retro terminal portal with an AI assistant](case-studies/terminal-portal.md)

## Run

Open `index.html`, or serve the folder: `python3 -m http.server`.

![Portrait](portrait-preview.png)

Security notes: [SECURITY.md](SECURITY.md).

---
Design and code: **Herman Hoffman** · [Hoffman Alternative](https://github.com/HOFFMAN-ALTERNATIVE)
