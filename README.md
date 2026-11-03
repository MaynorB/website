# Maynor's portfolio

A three-page portfolio built with Quarto's standard Flatly (light) and Darkly (dark) themes. The navbar toggle switches modes, and the initial mode follows the visitor's system preference.

## Local development

Install [Quarto](https://quarto.org/docs/get-started/) (the deployment workflow uses version 1.9.38). From this directory, run:

```sh
quarto preview
```

Quarto opens a local preview and refreshes it as source files change. To build without starting a preview:

```sh
quarto render
```

The generated website is in `_site/`. Generated HTML and `.quarto/` caches are ignored by Git.

## Editing

- Edit `index.qmd`, `projects.qmd`, and `contact.qmd` for page content, using Markdown.
- Edit `_quarto.yml` for shared navigation, metadata, theme, and footer.
- Edit `style.css` for custom styling; `favicon.svg` is the site icon.
- Link between pages using their `.qmd` filenames; Quarto generates `.html` links.

## Deployment

On a push to `main`, GitHub Actions installs Quarto, renders and checks the site, and deploys only `_site/` to GitHub Pages. The repository's Pages source should be **GitHub Actions**.

The public base URL is `https://maynorb.github.io/website/`. Quarto generates the sitemap from `website.site-url`; keep `robots.txt` in sync if the URL changes. Existing page URLs (`index.html`, `projects.html`, and `contact.html`) are preserved.
