# gender-equality-startistical-report

![Python](https://img.shields.io/badge/Python-3.11%2B-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebooks-F37626?style=for-the-badge&logo=jupyter&logoColor=white)
![pandas](https://img.shields.io/badge/pandas-Data%20Analysis-150458?style=for-the-badge&logo=pandas&logoColor=white)
![SciPy](https://img.shields.io/badge/SciPy-Statistical%20Testing-8CAAE6?style=for-the-badge&logo=scipy&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-Visualisation-11557C?style=for-the-badge)
![OECD](https://img.shields.io/badge/Data-OECD%20Gender%20Dashboard-0B5CAD?style=for-the-badge)

## The Gender Conversion Gap

Statistics project exploring whether stronger women's participation in STEM and digital skills is associated with stronger labour-market power outcomes across OECD countries.

The project focuses on the gap between **pipeline representation** and **labour-market outcomes**, with Estonia used as a country benchmark.

## Research Question

Do OECD countries with higher women’s STEM and digital participation also show stronger labour-market outcomes, such as lower gender wage gaps and higher representation of women in management?

## Project Outputs

- [Final analytical report](reports/The-Gender-Conversion-Gap-From-STEM-and-Digital-Participation-to-Labour-Market-Power.pdf)
- [Presentation](reports/The-Gender-Conversion-Gap-presentation.pdf)
- [Analysis-ready dataset](data/processed/gender_conversion_gap_latest.csv)
- [Data dictionary](data/processed/data_dictionary.csv)
- [Report figures](reports/figures)

## Data and Methods

The analysis uses OECD Gender Dashboard indicators collected through the OECD Data Explorer / SDMX API workflow.

Main sample:

- 38 OECD member countries
- Aggregate areas excluded from hypothesis testing
- Latest-available country-level indicators

Methods:

- Descriptive statistics and missingness checks
- Estonia versus OECD benchmark comparison
- Pearson and Spearman correlation tests
- Simple linear regression for bivariate hypothesis checks
- Holm adjustment for the two primary hypothesis tests

## Selected Visuals

<p align="center">
  <img src="reports/figures/fig03_estonia_vs_oecd_median_direction_adjusted.png" width="48%" alt="Estonia versus OECD median benchmark">
  <img src="reports/figures/fig05_hypothesis_results_pearson_summary.png" width="48%" alt="Hypothesis testing Pearson correlation summary">
</p>

## Key Findings

- The data do **not** support a simple story where STEM pipeline gains automatically translate into stronger labour-market power.
- H1 found partial support: women’s STEM graduate share is positively associated with women’s representation in senior and middle management, but the result is sensitive to influential observations.
- H2 was not supported: higher women’s STEM graduate share was not strongly associated with lower median gender wage gap indicator values.
- Estonia combines high women’s representation among tertiary STEM graduates with a high median gender wage gap indicator and below-median representation of women in senior and middle management.

## Recommendation Focus

The main recommendation is to move from pipeline-only monitoring to **conversion-layer monitoring**:

- STEM education to STEM-intensive employment
- Retention and promotion
- Pay transparency and pay audits
- Representation in senior and middle management

## Repository Structure

```text
gender-equality-statistical-report/
│
├── README.md
├── data/
│   ├── raw/
│   └── processed/
│
├── notebooks/
│   ├── 00_feasibility_and_data_contract.ipynb
│   ├── 01_exploratory_data_analysis.ipynb
│   ├── 02_hypothesis_testing.ipynb
│   └── 03_report_figures.ipynb
│
├── reports/
│   ├── The-Gender-Conversion-Gap-From-STEM-and-Digital-Participation-to-Labour-Market-Power.pdf
│   ├── The-Gender-Conversion-Gap-presentation.pdf
│   ├── figures/
│
└── references.md
```

## Limitations

- The analysis is cross-country and observational, not causal.
- Latest-available indicators are not always from the same year.
- Country-level data cannot track individual women from education into careers.
- The wage gap indicator is unadjusted and should not be read as equal pay for equal work.

## Tech Stack

Python, Jupyter Notebook, pandas, NumPy, SciPy, statsmodels, Matplotlib, OECD SDMX/API workflow.
