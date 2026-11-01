# codiscovery.ai

Source for [CoDiscovery.ai](https://codiscovery.ai). Static site, no build step, deployed on Netlify.

## Layout

| Path | What |
|---|---|
| `index.html` | Landing page. |
| `contrastive-discovery/` | Contrastive Discovery project page (`index.html`, `style.css`, `assets/`). |
| `contrastive-discovery/paper.pdf` | The paper; `/contrastive-discovery/pdf` serves it (`_redirects`, with `pdf/index.html` as fallback). |

## Run locally

```sh
python3 -m http.server 8000
# open http://localhost:8000/
```
