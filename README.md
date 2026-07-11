# LOE FAMILY EAT TOGETHER — Spin Wheel 🍽️🔵

A single-page spinner wheel for the family gathering. Add your own numbers or
names, spin the wheel, and it picks one. No build step — just one `index.html`
file, so it deploys straight to GitHub Pages.

## What it does

- Add any options yourself: numbers, names, menu items — type one and hit
  **Tambah**, or paste a comma-separated list.
- Quick presets: 1–6, 1–10, or example family names.
- Click the wheel's center hub to spin.
- Optional "buang yang menang" mode: removes the winner from the wheel after
  each spin, so you can use it to cycle through everyone's turn.
- Confetti burst + result banner when the wheel stops.
- Fully responsive (works fine on a phone at the dinner table) and respects
  reduced-motion settings.

## Deploy to GitHub Pages

1. **Create a new repository** on GitHub (public repos get free Pages
   hosting). Name it whatever you like, e.g. `loe-family-spinner`.

2. **Upload the files.** Easiest way if you're not using git locally:
   - Open your new repo on GitHub → **Add file → Upload files**
   - Drag in `index.html` (and this `README.md` if you want)
   - Commit directly to the `main` branch

   Or with git from your machine:
   ```bash
   git init
   git add index.html README.md
   git commit -m "Add LOE FAMILY spinner wheel"
   git branch -M main
   git remote add origin https://github.com/<your-username>/<repo-name>.git
   git push -u origin main
   ```

3. **Turn on GitHub Pages:**
   - In the repo, go to **Settings → Pages**
   - Under "Build and deployment", set **Source** to `Deploy from a branch`
   - Set **Branch** to `main` and folder to `/ (root)`
   - Click **Save**

4. **Wait ~1 minute**, then refresh that Pages settings page. It'll show your
   live URL, something like:
   ```
   https://<your-username>.github.io/<repo-name>/
   ```

That's it — share that link with the family group chat and it's ready for
the event.

## Editing later

Everything (markup, styles, logic) lives in `index.html` — no dependencies
to install. Open it in any text editor, tweak, and push the change; GitHub
Pages redeploys automatically within a minute or so.

Things you might want to tweak:
- Default starting options: search for `var options = ["1","2","3","4","5","6"];`
  near the top of the `<script>` block.
- Colors: the `:root { ... }` CSS variables near the top of the `<style>`
  block (`--sky-400`, `--sun-400`, etc.).
- Title/subtitle text: inside the `<header class="hero">` section.
