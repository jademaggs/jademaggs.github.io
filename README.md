# jademaggs.github.io

Personal website and professional portfolio for Dr Jade Maggs, Fisheries Scientist.

Built with [Quarto](https://quarto.org) and hosted on GitHub Pages.

## Structure

```
.
├── _quarto.yml          # Site configuration
├── index.qmd            # Home page
├── experience.qmd       # Career history, qualifications, consulting
├── research.qmd         # Research themes, output summary, selected publications
├── portfolio.qmd        # Worked analyses (in progress)
├── styles.css           # Custom styling
├── assets/              # PDFs and other static files
│   ├── jade_maggs_capability_statement.pdf
│   ├── jade_maggs_cv.pdf
│   ├── jade_maggs_cv_consulting.pdf
│   └── jade_maggs_publications.pdf
└── docs/                # Rendered site (GitHub Pages serves this)
```

## Local development

Install [Quarto](https://quarto.org/docs/get-started/), then:

```bash
quarto preview
```

## Deploying

```bash
quarto render
git add .
git commit -m "Update site"
git push
```

GitHub Pages serves from the `docs/` folder on the `main` branch.
