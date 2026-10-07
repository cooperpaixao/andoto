# andoto

Static site for andreotoo.com, served by the Cloudflare Worker `andreoto`
(also at andreoto.cooper-577.workers.dev). Plain HTML, no build step.

- `index.html`, `images/`, icons, `robots.txt`, `sitemap.xml`, `llms.txt`: the site.
- `_headers`: security and cache headers.
- `wrangler.jsonc`: Worker config; `.assetsignore` keeps repo files off the site.

Publishing: Cloudflare builds deploy every push to `main` (`npx wrangler deploy`).
Check locally with `npx wrangler@4 deploy --dry-run`.
