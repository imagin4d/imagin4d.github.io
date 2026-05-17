# imagin4d.github.io

Project page for **IMAGIN-4D: Image-Guided Controllable Interaction Generation**.

Paper: <https://arxiv.org/abs/2606.23675>

## Local preview

```
python -m http.server 8000
# open http://localhost:8000
```

## Layout

```
imagin4d_website/
  index.html
  static/
    css/      # bulma, fontawesome, index.css (from ECON template)
    js/       # bulma-carousel, bulma-slider, index.js
    figures/  # drop teaser.png and method.png here
    results/  # drop carousel slide images / gifs here
```

`academicons` (arXiv icon) and Google Fonts come from CDNs; everything else is
local so the page works offline once `static/figures/*` and `static/results/*`
are populated.

## What to edit in `index.html`

Search for `TODO` and bracketed `[...]` blocks:

- Title and venue (hero section)
- Teaser figure (`static/figures/teaser.png`)
- Pitch paragraph under the teaser
- Results carousel slides
- Abstract
- Summary Video iframe `src`
- Method figure (`static/figures/method.png`) and walkthrough
- BibTeX block

## Pushing to `imagin4d.github.io`

This is a **GitHub user/organization site**, so the repo must be named exactly
`imagin4d.github.io` and live on the `imagin4d` account.

```
git add .
git commit -m "Update project page"
git push -u origin main
```

In the repo's **Settings -> Pages**, confirm "Build and deployment ->
Deploy from a branch", branch `main`, folder `/ (root)`. The site goes live at
<https://imagin4d.github.io/> within ~1 minute.

## Template credit

CSS and carousel JS adapted from
[Yuliang Xiu](https://xiuyuliang.cn)'s [ECON](https://xiuyuliang.cn/econ/)
website template.
