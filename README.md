# Simple Galaga / Star Swarm

Kosmiczna gra arcade w HTML. Sterowanie: strzałki / A i D, spacja, P.

## Gra w przeglądarce
Pobierz `index.html` i otwórz w Chrome. Można też włączyć **Settings → Pages → Build and deployment → GitHub Actions**; workflow `Publish web game` opublikuje stronę. **Uwaga:** GitHub Pages dla prywatnych repozytoriów zależy od planu GitHub; opublikowana strona jest publiczna.

## Windows EXE
Po wypchnięciu tagu `v0.1.0` workflow `Build Windows EXE` zbuduje instalator Windows (.exe) i doda go do **Releases**. Można też uruchomić workflow ręcznie w **Actions** i pobrać EXE z **Artifacts**. Plik EXE jest instalatorem; po instalacji gra uruchamia się jako aplikacja Windows. Tauri używa systemowego WebView2 (na większości współczesnych Windows jest już obecny).

Lokalnie: Node.js 22, Rust i narzędzia C++ dla Windows; `npm install`, `npm run prepare:web`, `npx tauri build --bundles nsis`.

Grafika i dźwięki generowane są w kodzie; bez zasobów oryginalnej Galagi.
