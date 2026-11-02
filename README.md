# drbrandonfrye.com

Professional site for Dr. Brandon Frye — educator, school leader, and instructional designer
based in Washington, DC.

## How it is served

- **Host:** GitHub Pages, deploying from `main` at the repository root
- **Domain:** `drbrandonfrye.com`, registered at Namecheap
- **DNS:** four A records on the apex pointing at GitHub Pages, plus a `www` CNAME to
  `lawrencetotimeh.github.io`
- **Custom domain:** set by the `CNAME` file in this repo. Do not delete it.
- **HTTPS:** enforced, certificate issued by GitHub

## Files

| File | Purpose |
|---|---|
| `index.html` | The entire site. Self-contained: CSS inline, photos embedded as data URIs. |
| `CNAME` | Tells GitHub Pages which custom domain to serve. |
| `og-card.jpg` | 1200x630 link-preview image referenced by the Open Graph tags. |
| `apple-touch-icon.png` | Home-screen icon for iOS. |
| `robots.txt`, `sitemap.xml` | Search engine crawling and indexing. |

The page has no build step and no dependencies. Edit `index.html`, commit, push; Pages
rebuilds in under a minute.

## Things that will break the site if changed carelessly

- Deleting `CNAME` drops the custom domain back to `lawrencetotimeh.github.io/drbrandonfrye`.
- Renaming `og-card.jpg` breaks link previews; the filename is hard-coded in the meta tags.
- The `og:image` meta tag needs an absolute URL. A relative path will not work.
