<img src='logo/Hex.png' align="right" height="139" />

# Burnout Scale Validation – Psychometric Analysis in R <img src="https://media.giphy.com/media/1oGT95WukVFcRO1OFZ/giphy.gif" width="50">

[![](https://img.shields.io/badge/Language-R-blue)](http://cran.r-project.org/)

<sub>*Last updated 2025-06-17.*</sub>

This repository contains R code for evaluating the psychometric properties of a new burnout scale, developed specifically for psychologists. The analyses were conducted as part of my PhD research on work addiction, health, and wellbeing.

The code may serve as a useful starting point for researchers and students seeking to conduct their own scale validation studies using R and the [`lavaan`](http://lavaan.ugent.be/) package.

## 📊 Analyses Included

The following psychometric analyses were performed:

- **Descriptive Statistics**: Sample characteristics and burnout prevalence
- **Confirmatory Factor Analysis (CFA)**: Assessment of factorial validity using a second-order model
- **Inter-item Correlations**: Evaluation of relationships among items
- **Internal Consistency**: Cronbach’s alpha, McDonald’s omega, and Composite Reliability (CR)
- **Convergent Validity**: Using factor loadings and Average Variance Extracted (AVE)
- **Criterion-Related Validity**: Correlations with external measures (e.g., work engagement, depression, anxiety)
- **Measurement Invariance**: Configural, metric, and scalar invariance across gender

## :telescope: Overview

The repository is organised into the following sections:

TBC

## :scroll: Notes

This repository assumes basic competence in R (e.g., data importing, confirmatory factor analysis, basic plotting) and focuses specifically on the application of **confirmatory factor analysis (CFA)**, as well as **reliability and validity checks**. The content is designed to support practical implementation rather than provide in-depth theoretical coverage.

## :hammer_and_wrench: Setup

To run the code, you will need:

1. A dataset relating to one independent variable, two mediator variables and one dependent variable.
2. A fresh installation of [**`R`**](https://cran.r-project.org/) (preferably version 4.3.1 or above).
3. [RStudio IDE](https://www.rstudio.com/products/rstudio/download/) (optional but recommended).
4. Install the required packages by running:

   ```R
   # in alphabetical order:
   pkgs <- c("tidyverse", "psych","MVN", "easystats", "lavaan", "semTools","semPlot", "apaTables", "here" )

   install.packages(pkgs, repos = c("https://easystats.r-universe.dev", getOption("repos")))

<details>
<summary>
<i>Package Versions</i>
</summary>
   
Run on Windows 11 x64 (build 22621), with R version 4.4.2.

</details>

Feel free to adjust this based on your preferences and specific details about your code and setup.
