# Research Intranet

Static intranet site that mirrors the Hermes ↔ Antigravity research pipeline.

## Build

```bash
uv venv .venv --python 3.11
uv pip install --python .venv/Scripts/python.exe mkdocs mkdocs-material pymdown-extensions
.venv/Scripts/python.exe -m mkdocs build --clean
```

## Serve locally

```bash
.venv/Scripts/python.exe -m http.server 8765 --directory site
```

Then open `http://localhost:8765/`.

## Source data

All artifacts and raw intel live in `C:\Users\Phamd\Documents\research-pipeline\`.
The `docs/` tree here is regenerated from that source by reading the latest
research-pipeline state and writing mkdocs-friendly markdown.
