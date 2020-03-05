
<!-- README.md is generated from README.Rmd. Please edit that file -->
FragFrame\_1
============

<!-- badges: start -->
<!-- badges: end -->
The FragFrame\_1 repository includes R code and data to reproduce the analyses shown in the article

**A global synthesis reveals that ecosystem decay exacerbates biodiversity loss with habitat loss**

*by Jonathan M. Chase, Shane A. Blowes, Tiffany M. Knight, Katharina Gerstner and Felix May*

Here we give a brief overview on the code and data files in this repository

Data
----

There are two data files in data folder:

`fragSAD_predicts_ewers.csv`: This file contains the species abundance data and fragment areas for all studies

`new_meta_2_merge.csv`: This file contains the meta data for all studies

R scripts
---------

### Pre-processing files

`0_init_dirs_load_packages.R`: This script loads necessary R packages and sets up path and working directories. This set up needs to be adjusted for specific users and R sessions.

`0_preproc_wide_to_long_format.R`, `0_preproc_ewers_et_al_2007.R`, `0_preproc_predicts_data.R`: These three files do the pre-processing of raw data. Essentially, these three files create the data file `fragSAD_predicts_ewers.csv`, which is published in this repository. The single study data files that are the input for the pre-processing files are not published here and therefore, this files cannot be re-run as they are.

### Main analysis

`1_analysis_get_biodiv_new.R`: This file implements the first main part of the analysis, which includes the standardization and estimation of biodiversity parameters and the community dissimilarity partitioning. Based on the data in `fragSAD_predicts_ewers.csv`, this R-script calculates all biodiversity parameters for all fragments, as well as the incidence- and abundance-based turnover and nestedness components for all fragment pairs.

`2_`: these files do some preliminary visual inspection of the data.

`3_`: these files do the second main part of the analysis by fitting models to the standardized data.

`4_`: this files contain code to conduct visual inpsection of model fits (e.g., plots of residuals, markov chain inspection, posterior predictive checks).

`5_`: these files prepare coefficients and posterior distributions for plotting.

`6_`: these files plot results as they are presented in the main manuscript text.

`7_`: these files plot results as they are presented in the extended data section.
