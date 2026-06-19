# Guitar / Spoltore — Credits Constellation Shooter

A mobile-first browser game inspired by the end-credits minigame from *Super
Smash Bros.* — but the names flying across the screen are your **family
ancestry atlas**. Every surfaced relative, married-in spouse, possible lead,
notable historical figure, and surname/place variant from the atlas appears as
a target.

## Play

Open **`index.html`** in any browser. It's a single self-contained file — no
build step, no dependencies, no internet needed. To play on your phone, just
open the file (or host it anywhere static) and add it to your home screen.

## How it works

- **Tap a name** to fire the cannon and zap it. Multi-touch works — blast
  several at once.
- Names **fly in and take formations** each wave (ring, heart, star, spiral,
  family tree, diamond, twin columns, wave) with a dramatic camera zoom-punch.
- **Chain hits** to build a combo multiplier (up to ×5).
- **Clear an entire formation** before it drifts away for a big bonus.
- Score, accuracy, best combo, and a letter grade (D → S) at the end.
- Your best score is saved locally.

## Name categories (color-coded like the atlas legend)

| Color | Category | Points |
|-------|----------|--------|
| Blue | direct spine | 150 |
| Cream | collateral blood | 100 |
| Gray | married-in | 80 |
| Gold dashed | possible / unresolved lead | 120 |
| Rust | notable historical figure | 300 |
| Violet | surname / place lead | 90 |

## Tech notes

- Pure HTML5 Canvas + vanilla JS, ~1 file.
- Fixed 720×1280 virtual play-field, letterboxed to fit any screen, so layout
  is identical on every device.
- Camera with zoom / pan / screen-shake for the credits-sequence flourish.
- Procedural WebAudio sound effects (laser, explosion, combo, formation-clear),
  with a mute toggle. Audio starts on the first tap (mobile autoplay rules).
- Touch gestures (double-tap zoom, scroll, pinch) are suppressed so the canvas
  owns every tap.

The name data lives in the `RAW` array near the top of the `<script>` block in
`index.html` — edit it there to add, fix, or recolor any name.
