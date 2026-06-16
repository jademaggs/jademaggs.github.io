@README.md

## Claude-specific instructions

### Rendering workflow

The source files are `.qmd` files. Rendered HTML lives in `docs/` and is what GitHub Pages serves. When Quarto is not available to render, update both the `.qmd` source AND the corresponding file in `docs/` manually so they stay in sync.

### PDF assets

PDFs in `assets/` are the Quarto source copies. On `quarto render`, they are copied automatically to `docs/assets/`. If rendering manually, copy new PDFs to both locations.

Current assets:
- `jade_maggs_capability_statement.pdf` — linked from home page and portfolio page
- `jade_maggs_cv.pdf` — linked from About page
- `jade_maggs_publications.pdf` — kept as backup; citations are now rendered inline on the Publications page

### Publications page

The selected publications list in `publications.qmd` is sourced from the `curriculum_vitae` GitHub repo (`jademaggs/curriculum_vitae`, private), specifically `jade_maggs_publications.tex`. Update from there when new publications are added.

### Deployment

Edit `.qmd` files → `quarto render` → `git add` → `git commit` → `git push`. GitHub Pages serves from `docs/` on `main`.

Do not edit files in `docs/` directly unless Quarto cannot be run — always prefer re-rendering from source.
