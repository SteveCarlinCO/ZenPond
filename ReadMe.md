# Pond Life

A living pond ecosystem simulation — a game that plays itself. Seven koi, a frog, lily pads, dragonflies, falling leaves, wind gusts, and generative meditation music. Zero player input required after load.

![Pond Life](pond-favicon.svg)

## Run it

Open `index.html` in any modern browser. No build step, no dependencies.

Or serve it locally:

```bash
npx serve .
# or
python3 -m http.server
```

## Files

| File | What |
|------|------|
| `index.html` | Page shell, canvas, favicon |
| `pond_styles.css` | Layout and page styling |
| `pond_script.js` | The entire simulation (~1.1 MB, all logic + embedded sprites) |
| `*-sprite.png` | Source sprite assets (koi variants, frog frames, tree, rock, textures, dragonfly) |
| `pond-favicon.svg` | Lily pad favicon |

> **Note:** `pond_script.js` embeds all sprites as base64 data URIs, so the sim runs from the three core files alone. The loose PNGs are the source assets.

## Features

**Life**
- 7 koi (3 varieties: Kohaku, Sanke, Yamabuki) with hunt/pause/sink behaviors
- Frog with pad → swim → hop → return cycle, tongue-snatches flies
- 10 flies (landing, ripples, respawn)
- Dragonfly perched on a cattail tip (slow 33° rotation, shiny green-blue body)
- Click the water to drop food pellets — koi come to feed

**Environment**
- Falling autumn leaves (wind-blown, land with ripples, float then sink)
- Random wind gusts (15–45s, oscillating strength, sways grass/reeds/leaves)
- 3-cluster cattails, dense wild meadow grasses (6 types), medium grass carpet
- Wet-mud shoreline transition, dirt bank with pebbles, winding dirt path
- Depth-of-field haze, dappled light, lily pad shadows, underwater plants

**Ambience**
- Generative Web Audio meditation music (pad chords, chimes, water washes) — toggle with 🎵
- Zen speed toggle (0.7×) — 🧘 button

## Controls

| Action | Effect |
|--------|--------|
| Click water | Drop food pellets for koi |
| 🎵 button | Toggle generative music |
| 🧘 button | Toggle zen (slow-motion) speed |

Everything else runs itself.

## License

MIT — do what you want with it.
