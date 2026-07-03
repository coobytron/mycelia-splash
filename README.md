# Mycelia

A standalone WebGL splash page for an Art Director portfolio site.

**Hero line:**

> Hi, I’m an Art Director utilizing AI to create tooling.

This project is built as a single static `index.html` file so it can be hosted on GitHub Pages, Netlify, Vercel, Cloudflare Pages, or any static web host.

## Files

```text
mycelia-splash/
├── index.html      # Full splash page + WebGL garden app
├── README.md       # Project notes
├── DEPLOY.md       # GitHub Pages + Squarespace embed instructions
├── .nojekyll       # Keeps GitHub Pages from running Jekyll processing
└── .gitignore
```

## Local preview

From this folder, run:

```bash
python3 -m http.server 8080
```

Then open:

```text
http://localhost:8080
```

A local server is recommended because the page uses JavaScript modules and external Three.js imports.

## Deploy target

For GitHub Pages, keep the splash page named:

```text
index.html
```

That lets GitHub Pages load it as the homepage for the repository.

## Squarespace embed

Once this is live on GitHub Pages, copy the published URL into the iframe snippet in `DEPLOY.md`, then paste that snippet into a Squarespace Code Block on your splash/home page.
