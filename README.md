# Ranked Data Statistical Analysis

Statistical analysis of ranked survey responses from 41 faculty members, examining preferences among six job-related qualities: contract, salary, health care, workload, chair support, and travel budget.

## Project overview

The project explores how faculty respondents rank six job qualities, whether the rankings differ across educational groups, and how preference models describe the relative importance of the items.

This repository presents the **course project's analysis**, not a newly collected survey. The original dataset was used in a published ranked-data research example.

## Methods

- Descriptive statistics of ranked responses, including mean ranks and standard deviations
- Chi-square-based assessment of departures from equal mean ranks
- Group comparisons by degree, including chi-square, Fisher's exact test, and t-tests
- Unfolding multidimensional scaling (UMDS) with a configuration plot and Shepard plot
- Plackett–Luce preference model, worth parameters, deviance, and log-likelihood
- Pairwise comparison of salary and health care coefficients
- Quasi-standard errors for model coefficients
- Plackett–Luce trees exploring experience and degree as respondent covariates

## Repository structure

- `R/SDS_RankedData_final.R` — main analysis script
- `presentation/FINAL_PRESENTATION_NOTES.md` — final presentation results, group attribution and limitations (text companion; original PDF not redistributed)
- `DEPENDENCIES.md` — R package dependencies and setup notes
- `.gitignore` — excludes local history, generated files, and private data

## Presentation

See [the final presentation notes](presentation/FINAL_PRESENTATION_NOTES.md) for the submitted findings and group credits. The original slide deck is not redistributed because it includes student identification numbers.

## Running the analysis

1. Install R and the packages listed in [DEPENDENCIES.md](DEPENDENCIES.md).
2. Obtain the source survey dataset from the publication's supplementary materials, subject to its reuse terms.
3. Save the original Excel dataset as `data/pare-1331-finch.xlsx`.
4. Open the project folder as your working directory in R or RStudio.
5. Run `R/SDS_RankedData_final.R`.

The script loads `data/pare-1331-finch.xlsx`. The original submitted script used a root-level file path; the repository version uses the `data/` folder.

**Reproducibility note:** The code has been reviewed for organization and missing imports, but its full statistical execution and numerical outputs have not been independently verified in this repository. Some analyses (particularly small-group tests and tree models) require interpretation with care.

## Data and attribution

The faculty-ranking dataset is associated with Holmes Finch's paper, *An Introduction to the Analysis of Ranked Response Data* (2022), included as a reference in the original course materials. Consult the original publication and supplementary materials for the data source and reuse conditions. The dataset and article PDF are not redistributed here pending confirmation of their license.

The analysis code and project presentation were developed for a Statistics for Data Science course project by Ankit Kumar Bhagat, Fiza Naeem, and Ivane Maeva Nague. This repository does not claim ownership of the original research dataset or paper.

## Tools

R, readxl, pmr, PlackettLuce, prefmod, qvcalc, smacof, grid.
