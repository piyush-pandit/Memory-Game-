# Project Context

## What this repo does
This repository contains a browser-based Memory / Concentration card-matching game built with plain HTML, CSS, and JavaScript. The app lets players flip cards, match pairs, track moves and time, rate performance, and save top scores locally in the browser.

The main entry point is [memory-game.html](./memory-game.html). It includes:
- a 4x4 and 6x6 grid mode
- card flip animations and win detection
- move counter and timer
- star-based rating system
- localStorage-based best-score tracking
- keyboard and mouse support for accessibility
- responsive layout for desktop and mobile screens

## What it stands for
The folder name is `memory-game-GHCP`, but the project itself does not define a formal long-form acronym. Based on the naming pattern and the context of the repository, `GHCP` most likely refers to a GitHub Copilot-related project label or a Copilot practice session, rather than a product or domain name used in the app itself.

## Purpose and value
This is a lightweight front-end project meant to demonstrate:
- vanilla JavaScript game logic
- UI state management without external libraries
- responsive accessibility-friendly design
- browser-only persistence using localStorage

## How to run it
1. Open [memory-game.html](./memory-game.html) directly in a browser, or
2. serve the folder locally with:
   ```bash
   python3 -m http.server 8000
   ```
3. Visit `http://localhost:8000/memory-game.html`

## Key files
- [README.md](./README.md) — project overview and usage instructions
- [memory-game.html](./memory-game.html) — the full game implementation
