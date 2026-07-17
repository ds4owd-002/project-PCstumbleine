# Where Does the Time Go? A TDABC Analysis of Informal Pit Latrine Emptying in Mzuzu, Malawi

Capstone project for the Open Wash Data course (`ds4owd-002`), applying the R tidyverse to a Time-Driven Activity-Based Costing (TDABC) dataset from a doctoral study on informal pit latrine emptying ("gulper") services in Mzuzu, Malawi.

## Read the report

📄 **[View the rendered report](https://ds4owd-002.github.io/project-PCstumbleine/)** *(once GitHub Pages is enabled for this repo — see note below)*

Or browse the source: [`docs/index.qmd`](docs/index.qmd)

## Repository structure

- `data/raw/` — original, untouched TDABC observation files, one per ridealong session (`.csv`).
- `data/processed/` — cleaned, combined analysis-ready dataset (`processed_data.csv`), its data dictionary, and a README describing the cleaning process.
- `docs/` — the Quarto report (`index.qmd`), its bibliography (`bibliography.bib`), and the rendered HTML output once knitted.

## Enabling the live report link

This repo's `docs/` folder is a standard [Quarto](https://quarto.org/) output directory. To make the rendered HTML report viewable at a public link (rather than requiring a download):

1. In this repo, go to **Settings → Pages**.
2. Under **Build and deployment → Source**, choose **Deploy from a branch**.
3. Set **Branch** to `main` and the folder to `/docs`, then save.
4. GitHub will publish the contents of `docs/` at `https://ds4owd-002.github.io/project-PCstumbleine/`, which serves `docs/index.html` as the homepage.

This only needs to be done once; every time `docs/index.html` is re-rendered and pushed, the live link updates automatically.

## Data privacy

Session-level metadata (exact date, location, enumerator identity) is held privately outside this repository. See `data/processed/README.md` for details.

## Author

Padraic Casserly ([pcasserly@ethz.ch](mailto:pcasserly@ethz.ch)), ETH Zürich.
