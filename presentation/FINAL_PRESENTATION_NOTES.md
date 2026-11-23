# Final presentation — Statistics for Data Science

**Project:** An Introduction to the Analysis of Ranked Response Data  
**Academic year:** 2025/2026  
**Course:** Statistics for Data Science  
**Instructor:** Prof. Salvatore Ruggieri  
**Project group:** Ankit Kumar Bhagat, Fiza Naeem, Ivane Maeva Nague

This is a text companion to the group's final 15-page presentation (`SDS_pp-fina.pdf`). Student identification numbers have been omitted from the public version. The original PDF has not been uploaded here.

> The numerical values below are **reported in the submitted presentation**; they have not been independently reproduced by executing the R code.

## 1. Dataset

The analysis examines rankings from **41 non-tenure-track higher-education faculty members**. Respondents rank six job qualities: contract length, salary, health care plan, workload, chair support, and travel budget. Respondent covariates include years of experience and degree.

## 2. Analytical approach

The group organized the project around four questions:

1. Are the rankings systematic or random? — chi-square test.
2. How do respondents and job qualities relate in preference space? — unfolding multidimensional scaling (UMDS).
3. What is each item's relative worth? — Plackett–Luce model, first-place probabilities, and quasi-standard errors.
4. Do degree and experience change ranking patterns? — group tests, model comparisons, and Plackett–Luce trees.

## 3. Reported results

| Analysis | Reported result | Group interpretation |
| --- | --- | --- |
| Chi-square test | χ²(5) = 78.99, p < 0.001 | Rankings are not random |
| Fisher's exact test (degree) | p = 1 | No detected difference |
| Welch t-test (contract) | t = −0.274, p = 0.785 | No detected difference |
| Welch t-test (salary) | t = 0.138, p = 0.891 | No detected difference |
| UMDS | Stress ≈ 0.23 | A 2D preference representation was examined |
| Plackett–Luce model | Deviance = 447.69; residual df = 610; AIC = 457.69 | Baseline model |
| Salary vs health care | z = 3.00 | Salary ranked higher |
| Plackett–Luce tree | One node, no splits | No significant subgroup split detected |

### First-place probabilities (presentation, slide 9)

| Job quality | Probability |
| --- | ---: |
| Salary | 49.2% |
| Health care | 21.7% |
| Contract | 10.3% |
| Chair support | 9.3% |
| Workload | 6.3% |
| Travel budget | 3.2% |

### Model comparison (presentation, slide 11)

| Model | Reported AIC |
| --- | ---: |
| Baseline Plackett–Luce | 457.69 |
| PLMC + experience | 457.70 |
| PLMC + degree | 457.70 |

The group interpreted these AIC results as providing no meaningful improvement from the two covariates.

## 4. Difference from Finch (2022)

The presentation contrasts the group's tree-based analysis with the original paper's reported degree effect on contract rankings. The group reported that its ranking ordered-logit (ROL) attempt failed with a singularity error and that its Plackett–Luce tree analysis found no significant splits.

**These are different methods, not a direct replication of the same hypothesis test.** Failure to detect a split in a sample of 41 respondents does not establish that all respondents have identical preferences.

## 5. Limitations and interpretation notes

- Ordinal rankings show order, not the size of preference differences.
- The sample contains 41 respondents; subgroup analyses may have limited power.
- The presentation reports `1 − stress²` as a variance-explained measure for UMDS. This should not be treated as a universally established variance-explained statistic without checking the specific model definition.
- A deviance/df ratio below one alone does not establish adequate model fit.
- Reported model outputs and significance tests should be rerun before citing them as independently verified.
- The original research paper and dataset should be credited separately from this course project.

## 6. Source

Finch (2022), *An Introduction to the Analysis of Ranked Response Data*, *Practical Assessment, Research & Evaluation*, vol. 27. The group used the faculty-ranking example from this publication.
