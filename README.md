# imagin4d.github.io

Anonymous project page scaffold.

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

Author/affiliation blocks are pre-filled with anonymous placeholders. Leave
them as-is until the paper is de-anonymized.

## Pushing to `imagin4d.github.io`

This is a **GitHub user/organization site**, so the repo must be named exactly
`imagin4d.github.io` and live on the `imagin4d` account.

Anonymity warning: `git config --global user.{name,email}` is almost certainly
set to your real identity. Override it **per-repo** before the first commit so
the commit history does not leak it:

```
git init -b main
git config user.name  "imagin4d"
git config user.email "imagin4d@users.noreply.github.com"
git add .
git commit -m "Initial commit"

# Create the GitHub repo while signed in as imagin4d (browser is easiest for a
# fresh account), then:
git remote add origin git@github.com:imagin4d/imagin4d.github.io.git
git push -u origin main
```

In the new repo's **Settings -> Pages**, confirm "Build and deployment ->
Deploy from a branch", branch `main`, folder `/ (root)`. The site goes live at
<https://imagin4d.github.io/> within ~1 minute.

## Template credit

CSS and carousel JS adapted from a standard academic project-page template.
Restore a full credit line post-acceptance, when anonymity no longer applies.
