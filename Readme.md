 (cd "$(git rev-parse --show-toplevel)" && git apply --3way <<'EOF' 
diff --git a/README.md b/README.md
index 77b81a19fd643fb0da67193e2f33c0ce4041a330..159be6fabba34bd7a983481d5ce6d424f0272de7 100644
--- a/README.md
+++ b/README.md
@@ -19,25 +19,29 @@ Then open: `http://localhost:8080`
 ```bash
 npx serve .
 ```
 
 ## Deploy on GitHub Pages
 
 This repo includes a GitHub Actions workflow at:
 
 - `.github/workflows/deploy-pages.yml`
 
 ### One-time setup in GitHub
 
 1. Go to your repository **Settings → Pages**.
 2. Under **Build and deployment**, set **Source** to **GitHub Actions**.
 3. Push to `main` (or `master`).
 
 After a push, GitHub Actions will deploy the site automatically.
 
 ## Project structure
 
 - `index.html` – App shell
 - `src/styles.css` – Game styles
 - `src/game.js` – Core game logic
 - `src/levels.js` – Level definitions
 - `src/audio.js` – Sound effects
+
+## Bonus mini-game
+
+- `dap-game.html` – Quick-time-event dap game with player customization (names, colors, skin tones, hats).
 
EOF
)
