# Deploy to GitHub Pages + Embed in Squarespace

## 1. Create the GitHub repo

Create a new public GitHub repository. Suggested name:

```text
mycelia-splash
```

Do not initialize it with a README if you plan to push this prepared folder directly.

## 2. Push this folder from Terminal

Replace `YOUR_USERNAME` with your GitHub username:

```bash
cd mycelia-splash-github
git init
git add .
git commit -m "Add Mycelia AI tooling splash page"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/mycelia-splash.git
git push -u origin main
```

## 3. Turn on GitHub Pages

In the GitHub repo:

1. Go to **Settings**
2. Open **Pages** from the sidebar
3. Under **Build and deployment**, set **Source** to **GitHub Actions**
4. Save

This repository includes a GitHub Actions workflow that publishes only the static site files needed for Pages.

Your site will publish at something like:

```text
https://YOUR_USERNAME.github.io/mycelia-splash/
```

## 4. Add it to Squarespace

In Squarespace:

1. Open your splash/home page
2. Add a **Code Block**
3. Set it to **HTML**
4. Paste this code, replacing the iframe `src` with your GitHub Pages URL:

```html
<div class="ai-splash-frame-wrap">
  <iframe
    src="https://YOUR_USERNAME.github.io/mycelia-splash/"
    title="AI Tooling Splash Page"
    loading="eager"
    allow="fullscreen; autoplay"
  ></iframe>
</div>

<style>
  .ai-splash-frame-wrap {
    position: relative;
    width: 100vw;
    height: 100vh;
    margin-left: calc(50% - 50vw);
    overflow: hidden;
    background: #04080a;
  }

  .ai-splash-frame-wrap iframe {
    position: absolute;
    inset: 0;
    width: 100%;
    height: 100%;
    border: 0;
    display: block;
  }
</style>
```

## 5. Make it the Squarespace homepage

In Squarespace Pages, open the page settings for the splash page and set it as the homepage.

## Notes

- Use a real browser/incognito window to test the final Squarespace embed.
- Do not paste the entire `index.html` into Squarespace. Host it and iframe it.
- If GitHub Pages gives you a 404, confirm that the file is named `index.html`, the branch is `main`, and Pages is publishing from `/` root.
