# codiscovery.ai

Source for [CoDiscovery.ai](https://codiscovery.ai). Static site, no build step, deployed on Netlify.

## Layout

| Path | What |
|---|---|
| `index.html` | Landing page. |
| `contrastive-discovery/` | Contrastive Discovery project page (`index.html`, `style.css`, `assets/`). |
| `contrastive-discovery/paper.pdf` | The paper; `/contrastive-discovery/pdf` serves it (`_redirects`, with `pdf/index.html` as fallback). |
| `contrastive-discovery/assets/social-card.png` | 1200×630 link-preview image (`og:image`): the title over `teaser.png`. Regenerate it whenever the teaser changes. |

## Editing the Contrastive Discovery page

- **Colors.** `style.css` keeps paper Figure 1's colors as `--f-*` and `--pos/--flat/--neg` variables. Use them for data
  (belief bars, check/cross marks) and `--accent` for headings and links.
- **Scroll story** (`#problem`). What the pinned stage shows at each step is the `STATES` table in the script at the
  bottom of `index.html`. The stage's static markup is the last step, so the page reads correctly without JavaScript.
- **Explanation lists** (`<ol class="alts">`). Add `data-dir="pos"`, `"flat"`, `"neg"`, or `"curve"` to an `<li>` to give
  it the figure's color and mini-plot for that direction (higher / no difference / lower / nonlinear). Color follows
  meaning, not the H number.

## Run locally

```sh
python3 -m http.server 8000
# open http://localhost:8000/
```
