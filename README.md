# Card Sharks website

A small Jekyll site with HTML content and shared CSS. No JavaScript or local build step is required for publishing: GitHub Pages builds the site when you push.

## Editing content

- `index.html`: book description, cover, and deck details.
- `author.html`: author biography.
- `contact.html`: contact details (public email pending).

Each content file begins with a short YAML block between `---` lines. Keep `layout: default` and the `nav` key; edit `title` to change the browser-tab title. Everything below that block is the page content. Use `<p>...</p>` for paragraphs and `<h2>...</h2>` for section headings.

## Editing the shared structure

- `_layouts/default.html`: shared document structure, header, navigation, and footer. `{{ content }}` inserts each page’s content.
- `_config.yml`: site title, description, domain, and navigation labels/links.
- `styles.css`: layout, typography, and colors.
- `assets/`: book cover and card back.

Links use Jekyll’s `relative_url` filter so they respect `baseurl`.

## GitHub Pages

Keep Settings → Pages configured to Deploy from a branch, `main`, `/(root)`. Push the changes and GitHub Pages will run Jekyll automatically. Do not add a `.nojekyll` file: it disables template processing.

The existing `CNAME` file and custom domain `cardsharksbook.com` are preserved. Keep `baseurl: ""` for this custom domain. To switch back to the repository URL without a custom domain, remove the custom domain in GitHub settings and set `url` to `https://syenkoc.github.io` and `baseurl` to `/syenkoc`.

Opening source HTML directly in a browser will show unprocessed templates. Preview the published website after GitHub finishes building, or use a locally installed Jekyll to preview before publishing.
