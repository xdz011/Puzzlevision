# PUZZLEVISION — Mr. Puzzles Rate-O-Rama

A fan-made, single-file browser game built around **Mr. Puzzles** from SMG4 / Puzzlevision.

Rate his shows from 1 to 5 stars, watch his TV face react live, then hit **ACCEPT** and get
hunted through a fully 3D low-poly maze shot through a grimy bodycam lens.

No build step, no server, no internet required — everything is local.

---

## Quick start

1. Open the `mr-puzzles` folder.
2. Double-click **`index.html`** (Chrome, Edge or Firefox).
3. Rate a show, then press **ACCEPT**.

> A desktop browser with a mouse and keyboard is required for the maze
> (WebGL + pointer lock for mouse look).

---

## What's in it

### Rating screen
- 6 shows, each ratable 1–5 stars.
- His face changes with your average: furious skull → angry → disappointed → annoyed →
  pleased → losing it → perfection insanity.
- The whole UI re-themes per mood (accent colour, glow, speech bubble, meter, page siren).
- **Hidden minus star** on every row (nearly invisible until you hover): gives him a
  heartbroken crying face and unlocks the easiest maze.
- Undertale-style typewriter speech with per-character voice blips; click the bubble to skip.

### The maze (3D)
- Procedurally generated maze, first-person, pointer-lock mouse look.
- Mr. Puzzles is a **low-poly (~700 triangle) character** with articulated hips, knees,
  shoulders, elbows and wrists — flat-shaded faceting, show-accurate outfit
  (TV head, bowler hat, kinked antenna, bow tie, waistcoat, suspenders, puzzle pants,
  oversized gloves).
- Walk cycle is speed-driven: stride length derives from ground covered, so no foot-skate.
- **1–5 stars → he runs** at you (face escalates with difficulty).
  **Minus star → he walks**, crying, at the slowest speed.
- Difficulty scales maze size, hunter speed, fog density and player speed from your rating.

### Jumpscare
- **The camera never moves.** It is locked to where you were caught — verified 0.000 m drift —
  so it cannot fall, sink or clip. He lunges to you and presses his glass against the lens.
- "Swallowed" feeling comes from a pure lens zoom (FOV 105° → 38°), then a white flash,
  then the **TV dimension** where you must STRUGGLE three times to break out.

### Bodycam post-processing
Fisheye barrel distortion · chromatic aberration · vignette · procedural handheld
shake/breath · true 1×1 auto-exposure (eye adaptation) · motion blur · film grain ·
procedural lens dirt & smudges · depth-of-field from a real depth texture ·
censorship pixelation over his face · bloom + lens flare ghosts off the exit light ·
8×8 video-compression artifacts · HUD with REC, timecode, battery and signal.

### Adware (main page)
A permanently bobbing "TOTALLY NORMAL KEYBOARD" popup with a TV mascot, fake countdown and
dwindling stock. Closing it is harmless. Buying it corrupts the whole site: jittering
layout, crimson goo, and realistic eyes that blink and follow your cursor.

---

## Controls

| Action | Key |
|---|---|
| Move | `W A S D` / arrows |
| Look | Mouse (click once to lock) |
| Sprint | `Shift` |
| Pause / release mouse | `Esc` |
| Ready up / resume | Click the prompt |

---

## Difficulty

| Your average | Maze | Hunter | Face |
|---|---|---|---|
| minus star | smallest | walks, slowest | heartbroken, crying |
| 1–2 stars | large | runs, fastest | furious skull / insane |
| 3 stars | medium | runs | insane / crazy |
| 4–5 stars | small | runs | crazy |

---

## Files

```
mr-puzzles/
├── index.html      everything: markup, CSS, all game + shader code
├── three.min.js    vendored Three.js r149 (works offline)
└── README.md
```

Optional: drop a `mr-puzzles.png` (character art) next to `index.html` and it will appear
on the rating screen.

---

## Build

Current build string is shown in the footer of the page: **`BUILD v4.0`**.

If the footer shows an older version after an update, close every tab of the site and
re-open the file with `Ctrl + F5` — browsers cache `file://` pages aggressively.

---

## Credits & disclaimer

Fan project. **Mr. Puzzles / SMG4 / Puzzlevision belong to SMG4 / Glitch Productions.**
Not affiliated with or endorsed by them. No assets are redistributed except the
Three.js library (MIT licence).
