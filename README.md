# ⏱ Stopwatch

A sleek, minimal stopwatch web app with a live progress ring, lap tracking, and millisecond precision — built with pure HTML, CSS, and JavaScript. No dependencies, no build step.

---

## Features

- **Millisecond precision** — displays time down to `.000`
- **Animated progress ring** — SVG ring rotates once every 60 seconds, giving a visual pulse to the timer
- **Lap tracking** — record laps with individual split times and cumulative totals
- **Start / Stop / Reset** — clean controls with visual feedback
- **Zero dependencies** — single self-contained HTML file, works offline

---

## Usage

Just open `stopwatch.html` in any modern browser — no server or installation needed.

```
open stopwatch.html
```

### Controls

| Button | Action |
|--------|--------|
| **START** | Begin timing |
| **STOP** | Pause the timer |
| **LAP** | Record a lap (split + total shown) |
| **RST** | Reset everything to zero |

---

## How It Works

- Uses `requestAnimationFrame` for smooth, high-frequency updates
- Elapsed time is calculated via `Date.now()` deltas, not frame counting — so pausing and resuming stays accurate
- The SVG ring progress is derived from `elapsed % 60000` for a clean 60-second cycle
- Laps are stored in an array and rendered newest-first

---

## Browser Support

Works in all modern browsers (Chrome, Firefox, Safari, Edge). Requires no polyfills.

---

## File Structure

```
stopwatch.html   ← everything in one file (HTML + CSS + JS)
README.md
```

---

## Customization

All colors are defined as CSS variables at the top of the `<style>` block:

```css
:root {
  --bg: #0a0a0a;
  --accent: #e8ff47;   /* ring + running state color */
  --accent2: #ff4757;  /* stop button color */
  --text: #f0f0f0;
  --muted: #444;
}
```

Change `--accent` to any color to re-theme the whole app instantly.

---

## License

MIT — free to use, modify, and distribute.