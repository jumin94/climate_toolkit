# Climate Toolkit — Bottom-up approaches to climate evidence

Website for the climate toolkit developed by the [BASE initiative](https://baseinitiative.net/) (Fundación Avina) and the WCRP lighthouse activity [My Climate Risk](https://www.wcrp-climate.org/my-climate-risk).

The site is built with [MkDocs Material](https://squidfunk.github.io/mkdocs-material/) and published for free on GitHub Pages. Every page is a plain Markdown text file, so you can edit the toolkit without installing anything.

## How to edit a page (no installation needed)

1. Open the page on the website and click the pencil icon ("Edit on GitHub") at the top right, or browse to the file in [`docs/`](docs/) on GitHub.
2. Click the pencil icon on GitHub, make your changes, and click **Commit changes**.
3. Wait about a minute. The website updates automatically (you can follow progress in the **Actions** tab).

## Where things are

| What | File |
|---|---|
| Home page (introduction, sections 1–4) | `docs/index.md` |
| Who we are | `docs/about.md` |
| Modules 1–8 | `docs/modules/module-1.md` … `module-8.md` |
| Figures | `docs/assets/figures/` |
| Downloadable PDF | `docs/assets/downloads/climate-toolkit-base.pdf` |
| Menu, site title, links | `mkdocs.yml` |
| Colours | `docs/assets/stylesheets/extra.css` |

## Formatting cheat-sheet

Normal Markdown works: `## Heading`, `**bold**`, `[link text](https://…)`, `- bullet`.

The colour-coded boxes used in the printed toolkit are written like this (indent the content by 4 spaces):

```markdown
!!! definitions "Definitions"

    **Term:** explanation…

!!! faq "Frequently asked questions"
!!! howto "How-To guide"
!!! examples "Example"
!!! background "Background"
```

Use `???` instead of `!!!` to make a box collapsible.

A figure with a caption:

```markdown
<figure markdown="span">
  ![Short description for screen readers](../assets/figures/my-figure.png)
  <figcaption><strong>Figure 1.</strong> Caption text.</figcaption>
</figure>
```

To add a new figure, upload the image into `docs/assets/figures/` (GitHub: **Add file → Upload files**).

## Previewing changes on your own computer (optional)

```bash
python -m venv .venv
source .venv/bin/activate        # Windows: .venv\Scripts\activate
pip install -r requirements.txt
mkdocs serve                     # open http://127.0.0.1:8000
```

## First-time setup on GitHub

1. Create a new public repository on GitHub (e.g. `climate-toolkit`) and push this folder to it.
2. In the repository, go to **Settings → Pages** and set **Source** to **GitHub Actions**.
3. In `mkdocs.yml`, replace `YOUR-GITHUB-USERNAME` with the GitHub user or organisation name.
4. The site will be live at `https://jumin94.github.io/climate_toolkit/`.

A custom domain (e.g. `toolkit.baseinitiative.net`) can be added later under **Settings → Pages**.

## Note on versions

`requirements.txt` pins MkDocs below version 2.0 on purpose. MkDocs 2.0 is incompatible with the Material theme, so leave the pin in place unless you are migrating the site.
