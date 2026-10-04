# Sleep Data Analysis

A private R data-analysis project built around a structured sleep-quality dataset and a leakage-safe baseline classification workflow.

## Repository structure

```text
.
├── data/
│   └── sleep_dataset.csv
├── sleep_data_analysis.Rmd
├── sleep_data_analysis.Rproj
├── R-packages.txt
├── .gitignore
└── README.md
```

## Analysis

[`sleep_data_analysis.Rmd`](sleep_data_analysis.Rmd) now provides a reproducible baseline rather than leaving the repository as data-only scaffolding. It validates the `Q15` sleep-quality target, creates a stratified hold-out split and tunes a Ranger Random Forest through a tidymodels workflow.

Imputation, unknown/novel factor handling and near-zero-variance filtering are part of the workflow, so they are learned inside cross-validation folds rather than on the held-out test set.

## Working with the repository

1. Open [`sleep_data_analysis.Rproj`](sleep_data_analysis.Rproj) in RStudio.
2. Install packages listed in [`R-packages.txt`](R-packages.txt).
3. Run or knit [`sleep_data_analysis.Rmd`](sleep_data_analysis.Rmd).

The analysis uses the project-relative path `data/sleep_dataset.csv`.

## Scope

This is an exploratory sleep-quality classification project and is not a clinical diagnostic tool.
