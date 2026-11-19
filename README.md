# PUZZLEVISION — Mr. Puzzles Rate-O-Rama

A fan-made, single-file browser game built around **Mr. Puzzles** from SMG4 / Puzzlevision.

Rate his shows from 1 to 5 stars, watch his TV face react live, then hit **ACCEPT** and get
hunted through a television studio shot through a grimy bodycam lens.

No build step, no server, no internet required — everything is local.

---

## Quick start

1. Open the `mr-puzzles` folder.
2. Double-click **`index.html`** (Chrome, Edge or Firefox).
3. Rate a show, then press **ACCEPT**.

> A desktop browser with a mouse and keyboard is required for the studio
> (WebGL + pointer lock for mouse look).

---

## What's in it

### Rating screen
- 6 shows, each ratable 1 to 5 stars.
- His face changes with your average: furious skull, angry, disappointed, annoyed,
  pleased, losing it, perfection insanity.
- The whole UI re-themes per mood (accent colour, glow, speech bubble, meter, page siren).
- **Hidden minus star** on every row (nearly invisible until you hover): gives him a
  heartbroken crying face and unlocks the easiest studio.
- Undertale-style typewriter speech with per-character voice blips; click the bubble to skip.

### THE STUDIO
You wake in a television studio with no crew, no audience, and no wrap.
**It is a building, not a maze:** six-cell rooms on a lattice, joined by eight-unit-wide
dolly corridors. Rooms *repeat* — the same seven types cycle across the floor, so you keep
walking into the room you just left.

The seven repeating rooms:
- **Studio Floor** — empty stage, gaffer-tape X's, camera pedestals, a teleprompter scrolling nothing
- **Chroma-Key Stage** — walls and floor forced to that saturated, wrong green
- **Cyclorama** — seamless white curve, shadowless, maddening
- **Production Control** — vision-mixer desk with a sixteen-screen multiviewer tiling the same empty room
- **Master Control** — a wall of channels, all dead air, all colour bars, all slightly different
- **Green Room** — a couch, and a TV playing the Green Room
- **Cafeteria** — long steel tables, trays, and a row of warm automats

Always: red tally lights bolted at head height (*always recording*), a black iron lighting
grid overhead with fluorescent panels that hum in rows that never end, polished concrete
with expansion joints and cable runs, boom mics dangling like hanged things, IFB earpieces
coiled on a desk.

**The walls breathe.** Over the course of a run, flesh creeps up from the floor — a slow,
growing red growth. You never see it move, only the result.

### The hunter
- Low-poly (~700 triangles) character with articulated hips, knees, shoulders, elbows and
  wrists, flat-shaded faceting, and a show-accurate outfit: TV head, bowler hat, kinked
  antenna, bow tie, waistcoat, suspenders, puzzle-pattern trousers, oversized gloves.
- Walk cycle is speed-driven: stride length derives from ground covered, so there is no
  foot-skate.
- **1 to 5 stars: he runs** at you, face escalating with difficulty.
  **Minus star: he walks**, crying, at the slowest speed.
- Difficulty scales building size, hunter speed, fog density and player speed.

### Jumpscare
- **The camera never moves.** It is locked to where you were caught (0.000 m drift), so it
  cannot fall, sink or clip. He lunges to you and presses his glass against the lens.
- The "swallowed" feeling comes from a pure lens zoom (FOV 105 to 38 degrees), then a white
  flash, then the **TV dimension** where you must STRUGGLE three times to break out.

### Bodycam post-processing
Fisheye barrel distortion · chromatic aberration · vignette · procedural handheld
shake and breathing · true 1x1 auto-exposure (eye adaptation) · motion blur · film grain ·
procedural lens dirt and smudges · depth of field from a real depth texture with
**autofocus that racks onto Mr. Puzzles** so he is always sharp · bloom and lens flare
ghosts off the exit light · 8x8 video-compression artifacts · HUD with REC, timecode,
battery, camera and signal readouts.

### Adware (main page)
A permanently bobbing "TOTALLY NORMAL KEYBOARD" popup with a TV mascot, fake countdown and
dwindling stock. Closing it is harmless. Buying it corrupts the whole site: jittering
layout, crimson goo, and realistic eyes that blink and follow your cursor.

### Loot, inventory & combat
- **Item spots** are scattered through the studios and corridors. A spot has loot
  75% of the time; the tier then rolls at the pitched gates — Uncommon 50%,
  Rare 25%, Legendary 5%, **Secret 0.001%** — Common fills the rest.
- **Food** restores stamina and grants a timed speed boost, scaling with rarity
  (Stale Donut → Craft-Services Sandwich → Energy Drink → Director's Espresso →
  Secret: Puzzlevision Popcorn).
- **Weapons** (Common Stick → Uncommon Slingshot → Rare Hammer → Legendary Fire
  Axe / Prop Rifle → Secret Minigun / Chainsaw) all deal damage that scales with
  rarity; melee costs a little stamina, ranged guns aim down a cone.
- **Inventory caps at 3.** `E` grabs the nearest item, `1` `2` `3` select a slot,
  `F` eats food / readies a weapon, `LMB` attacks. Slots glow in the item's
  rarity colour.
- **Mr. Puzzles has HP** — the harder your rating, the tankier he is (140 → 500).
  A red HP bar appears over the studio once you draw blood; he staggers when hit
  and collapses for good at zero: **SHOW CANCELLED**.

### Stamina
- Sprinting drains it, everything else regenerates it.
- Below ~40% the bodycam darkens; below that it starts **flickering** like a
  dying battery. Eat something.

---

## Controls

| Action | Key |
|---|---|
| Move | `W A S D` / arrows |
| Look | Mouse (click once to lock) |
| Sprint | `Shift` (drains stamina) |
| Grab item | `E` |
| Use / eat / ready | `F` |
| Select slot | `1` `2` `3` |
| Attack | Left mouse button |
| Pause / release mouse | `Esc` |
| Ready up / resume | Click the prompt |

---

## Difficulty

| Your average | Building | Hunter | Face |
|---|---|---|---|
| minus star | smallest | walks, slowest | heartbroken, crying |
| 1 to 2 stars | large | runs, fastest | furious skull / insane |
| 3 stars | medium | runs | insane / crazy |
| 4 to 5 stars | small | runs | crazy |

---

## Files

```
mr-puzzles/
  index.html      everything: markup, CSS, all game and shader code
  three.min.js    vendored Three.js r149 (works offline)
  README.md
```

Optional: drop a `mr-puzzles.png` (character art) next to `index.html` and it will appear
on the rating screen.

---

## Build

Current build string is shown in the footer of the page: **`BUILD v4.37 • adware keyboard`**.

If the footer shows an older version after an update, close every tab of the site and
re-open the file with `Ctrl + F5` — browsers cache local pages aggressively.

---

## Credits and disclaimer

Fan project. **Mr. Puzzles / SMG4 / Puzzlevision belong to SMG4 / Glitch Productions.**
Not affiliated with or endorsed by them. No assets are redistributed except the
Three.js library (MIT licence).

