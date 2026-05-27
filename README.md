# Multinational Public Opinion on Race, Ethnicity, and Algorithmic Reform in Medicine

Reproducibility repository for the paper:

> Adibi A, Le KX, Pierson E, Diao JA, Esfandiari N, Carlsten C, Sadatsafavi M.
> *Multinational Public Opinion on Race, Ethnicity, and Algorithmic Reform in Medicine.*
> medRxiv 2026.05.15.26352687. <https://www.medrxiv.org/content/10.64898/2026.05.15.26352687v1>

## Overview

This repository contains the Quarto source needed to reproduce all tables, figures, and statistics reported in the manuscript. The de-identified survey dataset is archived on Zenodo at <https://zenodo.org/records/20403996> and is downloaded automatically when the manuscript is rendered. The study is a cross-sectional, multinational opt-in online survey (January 2026, n=994 eligible respondents from 43 countries) assessing public opinion on the use of race and ethnicity in clinical algorithms.

## Requirements

- [R](https://www.r-project.org/) (>= 4.5.2)
- [Quarto](https://quarto.org/) (>= 1.9.36)
- R packages: `tidyverse`, `ggthemes`, `gtsummary`, `flextable`, `ggalluvial`, `patchwork`, `UpSetR`

Install the required R packages:

```r
install.packages(c("tidyverse", "ggthemes", "gtsummary", "flextable",
                   "ggalluvial", "patchwork", "UpSetR"))
```

## Reproducing the manuscript

From the repository root:

```bash
quarto render manuscript.qmd
```

This regenerates `manuscript.html` along with all embedded tables and figures. To produce a Word document instead, render with the `docx` format (requires `custom-reference-doc.docx`):

```bash
quarto render manuscript.qmd --to docx
```

## Data

The de-identified survey dataset is archived on Zenodo <https://zenodo.org/records/20403996>

The `load-cleaned-data` chunk in [manuscript.qmd](manuscript.qmd) reads the CSV directly from this URL, so no manual download is required to render the manuscript.


## Citation

If you use this code or data, please cite the medRxiv preprint above.

## License

Code in this repository is released under the [MIT License](LICENSE). The survey data are shared for the purpose of scientific reproducibility; please cite the manuscript when using them.


