# ⚽ World Cup 2026 Predictor

A fun, single-page web app that lets you pick two nations and watch them battle it out in a physics-based mini football match. The winner is your World Cup 2026 prediction — decided entirely by marble-style ball physics and a rotating goal.

![World Cup 2026 Predictor](https://img.shields.io/badge/World%20Cup-2026-gold?style=flat-square)
![HTML5](https://img.shields.io/badge/HTML5-Canvas-orange?style=flat-square)
![No dependencies](https://img.shields.io/badge/dependencies-none-brightgreen?style=flat-square)

## Demo

Open `index.html` in your browser, or serve it locally:

```bash
# Python 3
python3 -m http.server 8080

# Node.js (npx)
npx serve .
```

Then visit [http://localhost:8080](http://localhost:8080).

> **Tip:** Serving over HTTP (rather than opening the file directly) ensures country flag images render correctly on the canvas.

## How it works

1. **Pick your teams** — Choose two nations from 40 World Cup contenders. Search by name to find your team quickly.

<img width="1274" height="754" alt="Screenshot 2026-07-15 at 10 01 48 pm" src="https://github.com/user-attachments/assets/5fdb5220-0d9a-4401-b252-2f2a3d34703e" />

2. **Kick off** — Two flag balls bounce around a circular arena. A goal opening rotates around the perimeter.
<img width="800" height="690" alt="Screenshot 2026-07-15 at 10 02 12 pm" src="https://github.com/user-attachments/assets/920aecb5-503d-4f91-b553-c1c7d0e3c75a" />

3. **Watch the match** — Balls collide with each other and the walls. Score by passing through the goal gap. The match runs for 90 simulated minutes (~70 seconds real time).
<img width="1071" height="704" alt="Screenshot 2026-07-15 at 10 07 47 pm" src="https://github.com/user-attachments/assets/220aae3d-7478-4e01-ad84-a0bd8f243659" />


4. **See the result** — Full-time score, winner announcement, and confetti for the champion.
<img width="1287" height="723" alt="Screenshot 2026-07-15 at 10 07 52 pm" src="https://github.com/user-attachments/assets/749b96ee-98bb-42c1-b550-6f7b822b99eb" />


## Features

- **40 nations** — Argentina, Brazil, France, Germany, USA, and more
- **Canvas physics** — Elastic wall bounces, ball-to-ball collisions, and a rotating goal post
- **Live scoreboard** — Real-time score and match timer with half-time whistle
- **Goal celebrations** — Animated overlay when a team scores
- **Results screen** — Winner highlight, final score, and confetti
- **Play again** — Reset and pick new teams without reloading
- **Responsive UI** — Dark football-themed design with search and country grid
- **Zero dependencies** — One HTML file, no build step, no npm install

## Tech stack

| Layer | Technology |
|-------|------------|
| Markup & styling | HTML5, CSS3 (custom properties, grid, animations) |
| Game engine | Vanilla JavaScript + HTML5 Canvas |
| Flags | [flagcdn.com](https://flagcdn.com) (loaded at runtime) |
| Physics | Custom 2D collision detection and inertia-based movement |

## Project structure

```
worldcup-demo/
├── index.html   # Complete app (HTML, CSS, and JavaScript)
└── README.md
```

Everything lives in a single self-contained file — easy to fork, deploy, or share.

## Deployment

This is a static site. Deploy to any static host:

- **GitHub Pages** — Push to `main`, enable Pages in repo settings, set source to root
- **Netlify / Vercel** — Drag and drop the folder or connect the repo
- **Any web server** — Upload `index.html` and serve as static content

## Customization

Open `index.html` and look for these constants in the `<script>` block:

| Constant | Default | Description |
|----------|---------|-------------|
| `matchDuration` | `70` | Real seconds for a full 90-minute match |
| `SPD` | `4.2` | Ball speed |
| `ROT` | `0.010` | Goal rotation speed |
| `GAP` | `0.34` | Goal opening size (radians) |

Add or remove countries in the `COUNTRIES` array at the top of the script.

## License

MIT — feel free to use, modify, and share.
