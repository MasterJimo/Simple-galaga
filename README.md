# Star Swarm 🚀

A free, browser-based arcade space shooter inspired by classic games. **Play instantly — no downloads or installation required.**

## Play online

🎮 **https://masterjimo.github.io/StarSwarm/**

GitHub Pages deploys the game automatically whenever the `main` branch changes. To enable it, open **Settings → Pages → Build and deployment** and select **GitHub Actions** as the **Source**.

Check deployment status at **Actions → Publish web game**. A green check mark means the latest deployment succeeded. If you just renamed this repository, the new Pages URL may need a fresh deployment before it works.

## Controls

| Key | Action |
| --- | --- |
| **← / →** or **A / D** | Move your ship |
| **Space** | Shoot |
| **P** | Pause / resume |
| **Enter** | Start / restart |

On wide screens, the **CONTROLS** panel appears to the right of the centered playfield, matching the blue **LEADERBOARD** panel on the left. It includes the **MUSIC** and **SFX** volume sliders, **START / RESTART**, **MUTE**, and a large uppercase keyboard guide. On narrow screens, both panels move below the game. Use the two sliders to adjust music and sound effects independently, or select **MUTE** to silence both.

## Gameplay

Shoot enemy formations, dodge incoming fire, and survive as many waves as possible. You have three lives. Higher waves become more challenging, and diving enemies are worth bonus points.

The game automatically scales to fit inside your browser window while preserving the whole playfield. For a larger view, maximize your browser window.

## Global leaderboard (Firebase)

The worldwide **TOP 10 leaderboard is always visible to the left of the game on wide screens**, without covering the playfield. On smaller screens, it moves below the game. Rankings update live from Firebase. After **GAME OVER**, enter a nickname (2–16 letters, digits, underscores or hyphens) in the leaderboard panel and select **Submit Score**. Your score and wave are captured automatically.

The game uses the Firebase project `starswarm-6589b` for Cloud Firestore and anonymous Firebase Authentication. Firebase is initialized directly in `index.html` with the web app's public configuration, so **no server, Firebase CLI, or build step is required** for the GitHub Pages game.

### Required Firebase Console setup

The following are one-time setup steps for the Firebase project owner:

1. In **Build → Firestore Database**, create a **Standard edition** database if one does not already exist. The database may start in **production mode**.
2. In **Build → Authentication → Sign-in method**, enable the **Anonymous** provider and select **Save**.
3. Open **Firestore Database → Rules** to review and manage the published security rules. Keep the existing restrictive rules that allow players to save only their own personal-best scores; use **Publish** after making changes. The rules are stored and enforced in **Firebase**, not GitHub. Do not replace them with permissive test-mode rules.
4. Load [StarSwarm online](https://masterjimo.github.io/StarSwarm/) (hard-refresh with **Ctrl + F5** if needed), finish a game, enter a nickname in the side panel, submit the score, and confirm it appears in the automatically updated **TOP 10**. A new deployment may take a little time.

### Moderate scores

In the Firebase Console, open **Firestore Database → Data → scores**. Each document is a player's best score. Select an inappropriate entry and use **Delete document**; you can delete all documents in that collection to reset the ranking. Regular anonymous players are not allowed to delete or overwrite lower scores under these Security Rules. Firebase Console owners can delete documents using administrative privileges.

### Security limitations

Scores are produced in the browser. Although the Security Rules validate types, score range, nickname format, ownership, and best-score-only updates, **they cannot prove that a displayed score was earned fairly**. Anonymous users can also create additional identities by resetting their browser. This is a casual leaderboard with basic protections, *not* an anti-cheat solution; robust validation would need a trusted backend. The game keeps running even when Firebase is unavailable, but score submission and the global leaderboard require Firestore rules and network access.

## Play locally

Download **`index.html`** from this repository and open it in Chrome, Edge, or Firefox. No local server or build tools are required.

## Technology

- HTML5 Canvas 2D for graphics
- Web Audio API for synthesized music and sound effects
- Vanilla JavaScript, HTML, and CSS
- No external assets or dependencies; visual designs and sounds are generated in code

**This project is browser-only.** It does not include a Windows EXE, an installer, or Tauri.
