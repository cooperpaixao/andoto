# andoto

Static site for andreotoo.com, served by the Cloudflare Worker `andreoto`
(also at andreoto.cooper-577.workers.dev). Plain HTML, no build step.

- `index.html`, `images/`, icons, `robots.txt`, `sitemap.xml`, `llms.txt`: the site.
- `fonts/`: Inter and Space Grotesk (latin, variable), served from the site. They are cached
  for a year, so give a changed font file a new name.
- `_headers`: security and cache headers.
- `wrangler.jsonc`: Worker config; `.assetsignore` keeps repo files off the site.

Publishing: Cloudflare builds deploy every push to `main` (`npx wrangler deploy`).
Pushes to other branches build a preview (`npx wrangler preview`, which needs the
`previews` block in `wrangler.jsonc`).
Check locally with `npx wrangler@4 deploy --dry-run`.
