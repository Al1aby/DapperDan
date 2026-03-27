 
 ### Option 1: Python
 
 ```bash
 python3 -m http.server 8080
 ```
 
 Then open: `http://localhost:8080`
 
 ### Option 2: Node
 
 ```bash
 npx serve .
 ```
 
 ## Deploy on GitHub Pages
 
 This repo includes a GitHub Actions workflow at:
 
 - `.github/workflows/deploy-pages.yml`
 
 ### One-time setup in GitHub
 
 1. Go to your repository **Settings → Pages**.
-2. Under **Build and deployment**, set **Source** to **GitHub Actions**.
-3. Push to `main` (or `master`).
+2. Under **Build and deployment**, set **Source** to **Deploy from a branch**.
+3. Choose branch **`gh-pages`** and folder **`/ (root)`**.
+4. Push to `main` (or `master`).
 
-After a push, GitHub Actions will deploy the site automatically.
+After a push, GitHub Actions will publish the site files to `gh-pages` automatically.
 
 ## Project structure
 
 - `index.html` – App shell
 - `src/styles.css` – Game styles
 - `src/game.js` – Core game logic
 - `src/levels.js` – Level definitions
 - `src/audio.js` – Sound effects
+
+## Bonus mini-game
+
+- `dap-game.html` – Two-player quick-time-event dap game (press `Space` to start) with multi-button sequences plus expanded customization and premium skin-pack preview options.
+- You can open `dap-game.html` directly from your filesystem (double-click) and it will run offline; a local/static server URL also works.
+- The page includes a built-in style fallback so character graphics still render even if your browser drops part of the advanced CSS.
