# EssayPilot

EssayPilot is a static product prototype for an AI-assisted study-abroad writing workspace. The current version is designed to be deployed directly with GitHub Pages.

## Files

- `index.html`: main entry page

## Local preview

Open `index.html` directly in a browser, or run a simple static server from the repo root.

Example with Python:

```bash
python -m http.server 8000
```

Then visit `http://localhost:8000`.

## GitHub Pages deployment

This repository can be deployed from the root of the `main` branch:

1. Push the latest commit to `main`
2. In GitHub repo settings, open `Pages`
3. Set source to `Deploy from a branch`
4. Choose branch `main` and folder `/ (root)`

After that, GitHub Pages will publish `index.html` automatically.
