# मोदक चोरी — Modak Chori!

A Vinayaka Chaturthi–themed endless runner for the Ganesh Chaturthi Game Design Contest.

## Story
Ganesha has snuck away on his vahana Mushak, racing down the golden slopes of
Kailash to gobble up as many modaks as he possibly can along the way. No one
chases him, nothing is at stake but his own appetite — just a joyful modak
run that ends the moment he stumbles on the trail.

## How to play
This is a **3-lane perspective runner** in the style of Temple Run / Subway
Surfers — a road stretches away toward the Kailash horizon, split into a
left, centre, and right lane.

- **Desktop:** ← → to switch lanes, ↑ / Space to jump, ↓ to duck.
- **Mobile:** swipe left/right to switch lanes, swipe up (or tap) to jump,
  swipe down to duck.
- **Rocks** — jump over them. **Icicles** — duck under them. **Boulders**
  span the whole lane — you can't jump or duck them, you have to switch lanes.
- Collect as many modaks as you can — they add to your score, with a sparkle
  burst on pickup.
- You have 3 lives (shown as modak icons top-right). Hit an obstacle and you
  lose one; lose all 3 and Ganesha takes a tumble, ending the run.
- The road speeds up the further you run. Score = modaks × 15 + distance × 1.5.
- Your best score is saved locally in the browser (`localStorage`) so it
  persists between visits on the same device/browser.

## Visual style
- Pseudo-3D perspective road with a vanishing point at the horizon, scrolling
  lane dividers, and obstacles/collectibles that scale up as they approach —
  the core visual trick behind Temple Run–style runners, done in plain 2D canvas.
- The trail itself is a grassy, rocky Kailash hillside path — snow stays up
  on the distant peaks only, with a forested foothill band, scattered
  wildflowers and grass tufts underfoot, and roadside garlands/flags
  alternating with small lotus-and-diya clusters and pine trees.
- Juice: dust kicked up under Mushak's feet while running, a screen shake +
  red flash on getting hit, a shrinking ground shadow that reads jump height,
  and a soft vignette for a more cinematic frame.
- A restyled UI in the spirit of richly painted temple art: glassmorphism
  panels with a small diya ornament and lotus corner flourishes, drifting
  petals behind the panel text, a festive gold/saffron gradient title, a
  pulsing call-to-action button, pill-shaped HUD badges, and a fading
  swipe/key hint shown at the start of each run.

## Running it
This is a fully static, self-contained web page — no build step, no external
dependencies, no network calls.

1. Open `index.html` directly in any modern browser, **or**
2. Serve the folder with any static file server, e.g.:
   ```
   npx serve .
   ```
3. To publish a live link for the contest (e.g. GitHub Pages):
   - Push this folder to a GitHub repo.
   - Settings → Pages → deploy from the `main` branch (root).
   - Share the resulting `https://<username>.github.io/<repo>/` link.

## Files
- `index.html` — **fully self-contained**: the page, styling, and game code
  are all inlined into this one file, so it runs correctly even if it's
  opened straight out of the zip (or from anywhere) without needing its
  sibling files to load. This is the file to open/host.
- `style.css` / `script.js` — the same styling and game code, kept here as
  readable source for editing. If you change something here, copy the
  updated content into the `<style>`/`<script>` blocks in `index.html` too
  (or just edit `index.html` directly — it's the one that actually runs).

## Tools used
- Vanilla HTML5 canvas, CSS, and JavaScript — no frameworks or external libraries
- Web Audio API for simple procedural sound effects (no downloaded audio assets)
- All visuals are drawn in code (canvas vector shapes) — no image assets, so there
  are no third-party asset licensing concerns

## Contest submission checklist
- [x] Clearly themed around Vinayaka Chaturthi (Ganesha, Mushak, modaks, Kailash)
- [x] Deity shown respectfully throughout — no harm, mockery, or disrespect
- [x] Complete loop: start screen → play → clear result (score/lives/distance) → game-over → play again
- [x] Works on mobile (touch buttons) and desktop (keyboard) browsers
- [x] No login, no passwords, no personal data collected
- [x] No campus-specific access restrictions — plain static link works for everyone
