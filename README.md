# InfiniForge — Canvas

A tiny drag‑and‑drop *Infinite Craft*-style toy that runs **entirely in the browser**.
- No backend.
- Optional local LLM via **LM Studio** (default `http://localhost:1234/v1`, model `gpt-oss-20b`).
- Early recipes are deterministic, later ones ask your model and cache the result.

## Run locally
```bash
python3 -m http.server 5500
# then open
http://localhost:5500/index.html?safe=1
```

## Using a local model (optional)
1. Open LM Studio → start the server (`:1234`) → load a model (e.g. `gpt-oss-20b`).
2. In the left panel set Base URL to `http://localhost:1234/v1` and Model to your model id.
3. Keep **Lock early canon** on. Toggle **Use model for unknowns** on/off as you like.

## Publish (GitHub Pages)
1. Create a repo and push this folder (index.html, README, LICENSE).
2. Settings → Pages → Build from **main / root**.
3. Share `https://YOURUSER.github.io/YOURREPO/`.
   *Note:* viewers won’t hit your local model; the page still works with canon-only mode.

## Credits
- UI + game glue: you.
- Local inference: LM Studio.
- Model: `gpt-oss-20b` (OpenAI Community OSS).

## Live demo

Once deployed via GitHub Pages, a live version of this app will be available at:

```
https://YOURUSER.github.io/infiniforge-canvas/
```

Replace `YOURUSER` with your GitHub username once Pages is enabled.
