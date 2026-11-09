# a-z-exe.github.io

Personal landing page for AmirHossein Zarei (A-z-exe).

- Static HTML, one page, no build step, no external requests.
- `Person` + `WebSite` JSON-LD, Open Graph and Twitter cards.
- Dark and light themes via `prefers-color-scheme`.

## Preview locally

```sh
cd a-z-exe.github.io
python -m http.server 8080
# open http://localhost:8080
```

## Deploy

The repository must be **public** and named exactly `a-z-exe.github.io`.

```sh
git init -b main
git add .
git commit -m "feat: personal landing page"
git remote add origin https://github.com/A-z-exe/a-z-exe.github.io.git
git push -u origin main
```

Then: Settings → Pages → Source: *Deploy from a branch* → `main` / `/ (root)`.
The site is live at <https://a-z-exe.github.io/>.

## After deploy

1. Add the URL to the GitHub profile (Settings → Profile → Website).
2. Add it as `sameAs` in JSON-LD once the custom domain is chosen.
3. In Google Search Console, add the property and submit `sitemap.xml`.
4. If a custom domain is used, add a `CNAME` file and update every absolute URL in `index.html` (canonical, Open Graph, JSON-LD).
