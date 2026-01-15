# MLDA Regression Discontinuity Design

This repository presents a fully reproducible regression discontinuity design (RDD) analysis estimating the causal effect of reaching the Minimum Legal Drinking Age (MLDA = 21) on mortality outcomes in the United States.

The project demonstrates modern applied causal inference methods using a canonical policy setting widely used in economics.

---

## Motivation

Legal access to alcohol changes discontinuously at age 21 in the United States. This institutional rule generates quasi-experimental variation that can be exploited to estimate the causal effect of alcohol access on mortality. The MLDA setting is a benchmark example in applied microeconometrics and is discussed extensively in *Mostly Harmless Econometrics*.

---

## Data

The analysis uses age-in-month mortality data compiled by Carpenter and Dobkin (2011), covering U.S. males from 1933–2004. Outcomes are measured as death rates per 100,000 population and are aggregated by age cell.

Data are downloaded automatically from Princeton University Press upon rendering the analysis.

---

## Empirical Strategy

We implement a sharp regression discontinuity design with age as the running variable and a cutoff at 21. Identification relies on the continuity of potential outcomes in age and the absence of manipulation of the running variable.

Estimation uses local linear regression with robust bias-corrected inference following Calonico, Cattaneo, and Titiunik (2014). The primary outcome is all-cause mortality, with external causes examined to assess mechanisms and internal causes used as a placebo outcome.

---

## Contents

- `rdd_analysis.qmd` – Main Quarto analysis
- `data/raw/` – Automatically downloaded raw data
- `renv.lock` – Reproducible R environment
- `rdd_analysis.html` – final output

---


