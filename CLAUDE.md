# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository

GitHub: https://github.com/SarikaPs/aitest (account: SarikaPs, branch: master)

After every change: commit with a clean message and push to `origin/master`.

## Project Structure

This repo contains self-contained browser games — each game is a **single HTML file** with all CSS and JavaScript inlined. No build tools, no package manager, no external dependencies.

```
tictactoe.html              — Two-player Tic Tac Toe with score tracking
magic-forest-counting.html  — Toddler counting game (Magic Forest theme)
```

## Running a Game

Open any HTML file directly in a browser:
```
start tictactoe.html
start magic-forest-counting.html
```

No server required.

## Code Conventions

**HTML file structure** (same pattern in every game):
1. `<head>` — single `<style>` block, all CSS inline
2. `<body>` — semantic HTML with `id`/`data-*` attributes, no class frameworks
3. `<script>` before `</body>` — all JS inline, no modules

**CSS**: CSS reset at top (`* { box-sizing, margin, padding }`), then layout, then component styles, then `@keyframes` at the bottom.

**JS**: State object at top → DOM refs cached in `init()` → pure functions for render/logic → event listeners wired in `init()` → `DOMContentLoaded → init()` at the bottom.

**Graphics**: All visuals are inline SVG — no image files. Claymation style uses layered ellipses + `radial-gradient` fills + multi-layer `box-shadow` for depth.

**Animations**: CSS `@keyframes` for idle/looping animations; Web Animations API (`element.animate()`) for one-shot triggered animations (e.g. apple bounce-in, apple fall-out).

**Viewport scaling** (`magic-forest-counting.html`): The scene is a fixed 390×844 logical canvas scaled via `transform: scale()` to fit any viewport — edit coordinates in that space.
