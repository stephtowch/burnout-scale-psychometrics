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

- **[01 Power Analysis](/R/01_Power_Analysis.R)**: Script for power analysis using the `pwr` package.
- **[02 SEM Model Assumptions](/R/02_SEM_Model_Assumptions.R)**: Script for data wrangling and assumptions testing using `dplyr`, `knitr`, `lavaan`, `lavaanPlot`, `mvnormalTest`, and `tidyr`.
- **[03 SEM (Latent Variables) Two-Mediator Serial Mediation](/R/03_SEM_(Latent_Variables)_Two-Mediator_Serial_Mediation.R)**: Script for actual SEM analysis using `lavaan`, `lavaanPlot`, and `semPlot`.
- **[04 Careless Longstring](/R/04_Careless_Longstring.R)**: Script to detect careless participants within the dataset using the `careless` package.
- **[05 Univariate Outliers](/R/05_Univariate_Outliers.R)**: Script to detect univariate outliers within the dataset using z-scores  the `dplyr` package.
- **[06 Convert IP Address to Country and plot on a map](/R/06_Convert_IP_Address_to_Country_and_plot_on_map.R)**: Script for converting IP addresses to countries and plotting on a map (requires loading Python in R).**
- **[07 Reliability](/R/07_Reliability_(Cronbach's_Alpha_and_McDonald's_Omega_Coefficients).R)**: Script for calculating Cronbach's Alpha and McDonald's Omega coefficients using the `psych` package.
- **[08 Descriptive Statistics](/R/08_Descriptive_Stats.R)**: Script for calculating descriptive statistics including min, max, mean using summary() function, as well as frequencies and correlation matricies using the `psych` package as well as the apa.cor.table() function from the `apaTables` package.

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
   pkgs <- c(
  "tidyverse", "psych",       # Basic tools
  "MVN", "easystats",         # Checking data
  "lavaan",                   # Building models
  "semTools",                 # Checking models
  "semPlot",                  # Visualisation
  "apaTables",                # Reporting
  "here"                      # File finder
   )

   install.packages(pkgs, repos = c("https://easystats.r-universe.dev", getOption("repos")))

<details>
<summary>
<i>Package Versions</i>
</summary>
   
Run on Windows 11 x64 (build 22621), with R version 4.4.2.

</details>

Feel free to adjust this based on your preferences and specific details about your code and setup.
