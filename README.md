# Stopwatch

A minimal, dark-themed stopwatch web app built with vanilla HTML, CSS, and JavaScript.

## Features

- **Start / Stop** — Toggle the timer with the main button
- **Lap tracking** — Record lap splits with the LAP button; each lap shows its split time and cumulative total
- **Reset** — Instantly clear the timer and all recorded laps
- **Animated progress ring** — A circular SVG ring completes one rotation every 60 seconds, giving a visual pulse to the elapsed time
- **Millisecond precision** — Displays time down to the millisecond using `requestAnimationFrame` for smooth updates

## Usage

Open `index.html` in any modern browser — no build step or dependencies required.

| Button | Action |
|--------|--------|
| **START / STOP** | Begins or pauses the timer |
| **LAP** | Records a lap (also works when paused to record a final split) |
| **RST** | Resets everything to zero |

## Tech Stack

- Plain HTML5, CSS3, and JavaScript (no frameworks)
- Fonts: [Bebas Neue](https://fonts.google.com/specimen/Bebas+Neue) & [DM Mono](https://fonts.google.com/specimen/DM+Mono) via Google Fonts
- Timing: `Date.now()` diff with `requestAnimationFrame` for accurate, smooth rendering

## Browser Support

Works in all modern browsers (Chrome, Firefox, Safari, Edge). Requires an internet connection to load Google Fonts; the layout degrades gracefully to system monospace fonts without it.
