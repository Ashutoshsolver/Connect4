# Connect4

A free, single-file, browser-based Connect Four game. Play against a computer opponent (three difficulty levels) or pass-and-play with a friend on the same device. No build step, no dependencies, no download — just open the HTML file.

**Author:** Ashutosh Shukla

## Features

- **Two game modes**
  - **Vs Computer** — you play Red, the computer plays Yellow.
  - **Play with Friend** — local pass-and-play, Player 1 (Red) vs Player 2 (Yellow).
- **Three AI difficulty levels**
  - **Easy** — computer picks a random valid column.
  - **Medium** — computer takes an immediate win if available, blocks your immediate win, otherwise plays randomly.
  - **Hard** — computer uses a minimax search with alpha-beta pruning (depth 4) and a positional heuristic (center-column control + window scoring) — a tough opponent.
- **Persistent stats** — win/loss/draw records for both "Vs Computer" and "Vs Friend" are saved locally and reloaded on your next visit.
- **Live in-match scoreboard** — tracks the score of the current session's round.
- **Animated gameplay** — discs drop with an animated fall, winning discs get a highlighted glow, and a column-hover indicator helps you aim.
- **Optional ambient music** — a lightweight generated tone loop (Web Audio API) toggled with the speaker button, no audio files required.
- **Mobile-friendly UI** — responsive layout, touch-optimized controls, safe-area padding for notched devices.
- **SEO / sharing metadata** — includes Open Graph, Twitter Card, and schema.org structured data for link previews and search indexing.

## Getting Started

No installation required.

1. Download or clone this repository.
2. Open `connect4.html` directly in any modern web browser (Chrome, Firefox, Safari, Edge).

That's it — the entire game (HTML, CSS, and JavaScript) lives in a single file.

### Hosting it online

Since it's a static file, you can deploy it anywhere that serves static content — GitHub Pages, Netlify, Vercel, or any basic web server. No server-side code or build tooling is needed.

## How to Play

1. From the home screen, choose a **difficulty** (only relevant for Vs Computer) and tap **Play vs Computer** or **Play with Friend**.
2. Tap/click a column on the board to drop your disc into the lowest open slot.
3. Players alternate turns (Red goes first). Line up **four discs in a row** — horizontally, vertically, or diagonally — to win.
4. If the board fills up with no winner, the round ends in a draw.
5. After a round, use **New Round** to keep the match score and play again, or **Home** to return to the main menu.

## Project Structure

This is a single self-contained file:

```
connect4.html   # All markup, styles (CSS custom properties/variables), and game logic (vanilla JS)
```

Internally, the script is organized into clear sections:

| Section | Responsibility |
|---|---|
| Persistence | Load/save win-loss-draw stats via `window.storage` |
| Navigation | Switching between the Home and Game screens |
| Difficulty | Difficulty selector state and UI hints |
| Music | Web Audio API ambient tone loop |
| Board logic | Board state, win detection, and the AI (random / heuristic / minimax) |
| Rendering | Drawing the grid, animating disc drops, turn indicator, scoreboard |
| Game flow | Starting a match, placing discs, handling round-end overlays |

## Tech Stack

- **HTML5** for structure and metadata (SEO, Open Graph, Twitter Card, JSON-LD).
- **CSS3** with custom properties for theming, CSS Grid for the board, and keyframe animations.
- **Vanilla JavaScript** (no frameworks or libraries) for all game logic, including a minimax + alpha-beta pruning AI.
- **Web Audio API** for the optional ambient background music.
- **Google Fonts** (`Baloo 2`, `Inter`) loaded via `@import`.

## Browser Support

Works in any modern browser that supports CSS Grid, CSS custom properties, and the Web Audio API (all current versions of Chrome, Firefox, Safari, and Edge).

## License

No license specified. Add one (e.g. MIT) if you intend to share or accept contributions.
