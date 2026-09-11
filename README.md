# Little Lemon 🍋

A simple, static multi-page website for **Little Lemon**, a Mediterranean restaurant. Built with plain HTML5 and CSS3 — no frameworks, no build step.

## Pages

| Page | File | Description |
|---|---|---|
| Home | `index.html` | Hero banner, menu/booking/hours highlights |
| Menu | `menu.html` | Menu item cards with photos and prices |
| Book | `book.html` | Reservation form |
| About | `about.html` | Restaurant story |
| — | `home.html` | Redirects to `index.html` (kept for backward-compatible links) |

## Project structure

```
little-lemon/
├── index.html
├── home.html
├── menu.html
├── book.html
├── about.html
├── style.css
├── README.md
└── img/
    ├── logo.png
    ├── logo1.png
    ├── logo-horizontal-yellow.png
    ├── logo-stacked-yellow.png
    ├── lemon-icon-yellow.png
    ├── lemon-icon-green.png
    ├── pasta.jpeg
    └── pastaa.jpeg
```

## Running it locally

No build tools needed. Just open `index.html` in a browser, or serve it locally:

```bash
# Python 3
python3 -m http.server 8000
# then visit http://localhost:8000
```

## Pushing to GitHub

1. **Create a new repository** on GitHub (e.g. `little-lemon`) — don't initialize it with a README, since you already have one.

2. **Initialize git locally** in this folder and push:

   ```bash
   cd little-lemon
   git init
   git add .
   git commit -m "Initial commit: Little Lemon site"
   git branch -M main
   git remote add origin https://github.com/<your-username>/little-lemon.git
   git push -u origin main
   ```

3. If you already have a git repo and this is an update:

   ```bash
   git add .
   git commit -m "Fix image paths, add responsive design and missing pages"
   git push
   ```

## Live preview with GitHub Pages

1. On GitHub, go to your repo → **Settings → Pages**.
2. Under **Build and deployment → Source**, choose **Deploy from a branch**.
3. Under **Branch**, select `main` and folder `/ (root)`, then **Save**.
4. Wait ~1 minute, then your site will be live at:

   ```
   https://<your-username>.github.io/little-lemon/
   ```

   GitHub will show you this exact URL at the top of the Pages settings once it's deployed.

5. Any time you `git push` new changes to `main`, GitHub Pages redeploys automatically within a minute or two.

### Alternative live previews

- **Netlify / Vercel**: drag-and-drop the whole folder onto [app.netlify.com/drop](https://app.netlify.com/drop) for an instant live URL, no git required.
- **VS Code Live Server extension**: right-click `index.html` → "Open with Live Server" for local hot-reload while editing.

## Notes on what was fixed

- All image paths now correctly point to the `img/` folder (they were broken before).
- `home.html`, `menu.html`, `about.html`, `book.html` were empty — now built out with matching structure/styling.
- Fixed invalid `text-shadow` CSS declaration.
- Added a mobile-responsive layout (`@media` breakpoint at 700px).
- Added `<meta name="description">` tags for basic SEO.
- Diversified image `alt` text for accessibility.
