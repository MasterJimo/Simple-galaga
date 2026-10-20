# Star Swarm 🚀

**Star Swarm** is a free, single-player arcade space shooter for desktop and mobile browsers. Pilot your ship, dodge enemy attacks, clear increasingly challenging waves and try to beat your high score.

## How to play

1. Open the game and press **Enter** or **START / RESTART** (on mobile, tap the game).
2. Move left or right, shoot enemy ships and avoid enemy bullets and diving attacks.
3. Destroy every enemy to advance to the next wave. Survive as long as you can!

### Controls

| Action | Keyboard | Phone / tablet |
| --- | --- | --- |
| Move left / right | **← / →** or **A / D** | **◀ / ▶** |
| Shoot (hold to repeat) | **Space** | **FIRE** |
| Start / restart | **Enter** or **START / RESTART** | Tap to start; **START / RESTART** to restart |
| Pause / resume | **P** or **PAUSE / RESUME** | **PAUSE / RESUME** button |

### Game rules and settings

- Start with **3 lives**. Enemy contact or a projectile costs a life.
- Formation enemies give **50, 60, 80 or 100 points** depending on their row; diving enemies give **150 points**.
- Use **SOUNDTRACK** to select one of 10 tracks. **MUSIC**, **SFX** and **MUTE** control the audio.
- The selected soundtrack is remembered in browser storage. There is no online leaderboard.

See [About & How to Play](about.html) for additional details.

## Assets and Credits

The currently tracked game files contain **no downloaded sprite sheets, image packs, music files or sound-effect samples**. The ships, enemies and effects are rendered directly by the game's code, while its 10 selectable music tracks and sound effects are synthesised live in the browser.

| Asset / contribution | Credit | Location / source |
| --- | --- | --- |
| Game and project | **MrJim** ([MasterJimo](https://github.com/MasterJimo)) | [`index.html`](index.html); [`about.html`](about.html) |
| Spaceship, enemies, bullets, particles and starfield | Programmatic graphics in the Star Swarm project (HTML Canvas); no third-party image files identified | [`index.html`](index.html), especially `drawShip()` and `draw()` |
| All 10 selectable in-game soundtracks — Classic Arcade, Neon Horizon, Reactor Rush, Bass Overdrive, Cosmic Pulse, Laser Storm, Hyperdrive, Dark Orbit, Pixel Uprising and Final Assault | Original procedural music implemented in the game using the browser's Web Audio API; no downloaded music tracks | [`index.html`](index.html), `tracks`, `scheduleMusicStep()` and related functions |
| Shooting, hits, damage and wave sound effects | Synthesised using Web Audio API; no external SFX files | [`index.html`](index.html), `tone()` |
| Arcade hub illustrations | Inline SVG artwork in this project; no third-party image assets identified | [`arcade/index.html`](arcade/index.html) |

**Asset source note:** No other third-party asset sources or download credits are identified in the tracked repository files. If new assets are added later, their creator, source URL, license and local file path should be documented here.

## Play and project

- **Source:** [GitHub — MasterJimo/Star-Swarm](https://github.com/MasterJimo/Star-Swarm)
- **Play:** Open the deployed site or run [`index.html`](index.html) in a modern web browser.
- **Privacy:** [Privacy Policy](privacy.html)
