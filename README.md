# a-z-exe.github.io

Personal site of AmirHossein Zarei (A-z-exe), in English and Persian.

- Static HTML, no build step, no external requests, no trackers.
- `/` — English profile; `/fa/` — Persian profile; `/card.html` — printable 85 × 55 mm card.
- `Person` + `WebSite` + `ProfilePage` JSON-LD, Open Graph and Twitter cards.
- `hreflang` pairs (`en`, `fa-IR`, `x-default`) on both pages and in `sitemap.xml`.
- Dark and light themes via `prefers-color-scheme`.

## Files

```
index.html              English profile
fa/index.html           Persian profile (RTL)
card.html               digital + printable business card (noindex)
portrait.jpg            stylized portrait used in the hero and schema
og.jpg                  1200 × 630 share image
og-source.html          source layout used to render og.jpg (noindex)
sitemap.xml, robots.txt
amirhossein-zarei.vcf   contact file
card-qr.png             QR code for the site
```

## Preview locally

```sh
python -m http.server 8080
# open http://localhost:8080
```

Use a server rather than `file://` so the root-absolute paths on `/fa/` resolve.

## Deploy

The repository must be **public** and named exactly `a-z-exe.github.io`; Pages serves `main` / root.
Live at <https://a-z-exe.github.io/>.

## SEO checklist

Done in this repo:

1. Unique titles and descriptions per page, canonical URLs, `hreflang` pairs.
2. `Person` schema with name variants (`Amirhossein Zarei`, `Amir Hossein Zarei`, `امیرحسین زارعی`) and `sameAs` profiles.
3. Persian page carries the name in an `<h1>` and throughout the copy.
4. `sitemap.xml` lists both pages with language alternates; `robots.txt` points to it.

Manual, once:

1. Google Search Console → add `https://a-z-exe.github.io/` → verify → submit `sitemap.xml`.
2. URL Inspection → request indexing for `/` and `/fa/`.
3. GitHub profile → Settings → Website: `https://a-z-exe.github.io/`.
4. Keep repository READMEs linking to the site (genuine, owned links).
