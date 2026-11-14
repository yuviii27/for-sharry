# for Sharmin

A single, self-contained web page. One file, no build step, no dependencies.

## Files

- `index.html` — the whole thing (HTML + CSS + JS, all inline)

That's it. Everything — the fonts fallback, the self-drawing web, the 3D gift
box — lives inside that one file.

## Deploy to GitHub Pages (3 steps)

1. Create a new repository on GitHub (e.g. `for-sharmin`). Keep it **public**
   so Pages can serve it.
2. Upload `index.html` (and this README) to the repository — or push from a
   local clone:
   ```bash
   git init
   git add index.html README.md
   git commit -m "add the page"
   git branch -M main
   git remote add origin https://github.com/<your-username>/<repo>.git
   git push -u origin main
   ```
3. On GitHub: **Settings -> Pages -> Source: Deploy from a branch ->
   Branch: `main` / `root` -> Save.**

Your page goes live in about a minute at:

```
https://<your-username>.github.io/<repo>/
```

## Local preview

Just open `index.html` in a browser. Or serve it:

```bash
python3 -m http.server 8000
# then open http://localhost:8000
```

## Notes

- Works offline after first load; the only external request is Google Fonts
  (with system-font fallbacks if it fails).
- The 3D box at the bottom opens on click, tap, Enter, or Space.
