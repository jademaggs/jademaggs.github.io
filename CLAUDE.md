@README.md

## Claude-specific instructions

### Rendering workflow

The source files are `.qmd` files. Rendered HTML lives in `docs/` and is what GitHub Pages serves. When Quarto is not available to render, update both the `.qmd` source AND the corresponding file in `docs/` manually so they stay in sync.

**Quarto must be run via PowerShell, not the Bash tool.** Use `quarto render` in a PowerShell command (it will not be found by Bash). After rendering, commit the updated `docs/` files.

### PDF assets

PDFs in `assets/` are the Quarto source copies. On `quarto render`, they are copied automatically to `docs/assets/`. If rendering manually, copy new PDFs to both locations.

Current assets:
- `jade_maggs_capability_statement.pdf` (linked from home page and portfolio page)
- `jade_maggs_cv_consulting.pdf` (linked from Experience page; the CV that downloads when visitors click "Download CV")
- `jade_maggs_cv.pdf` (academic CV, kept in assets but not currently linked from any page)
- `jade_maggs_publications.pdf` (kept as backup; citations are now rendered inline on the Research page)

### Research page

`research.qmd` (renamed from `publications.qmd`) is ordered: Research themes, then Research output summary table, then Selected publications. The selected publications list is sourced from the `curriculum_vitae` GitHub repo (`jademaggs/curriculum_vitae`, private), specifically `jade_maggs_publications.tex`. Update from there when new publications are added.

### Styling

The site uses Bootstrap Flatly theme with a custom teal accent colour `#0f6e56` defined in `styles.css`. All headings, navbar borders, and buttons use this colour. The darker hover variant is `#085041`. Do not introduce other accent colours.

### Deployment

Edit `.qmd` files → `quarto render` → `git add` → `git commit` → `git push`. GitHub Pages serves from `docs/` on `main`.

Do not edit files in `docs/` directly unless Quarto cannot be run; always prefer re-rendering from source.
