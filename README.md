# DNA Metabarcoding Highlights Cyanobacteria as the Main Source of Primary Production in a Pelagic Food Web Model: Supplementary Data Analysis

***Andreas Novotny, Baptiste Serandour, Susanne Kortsch, Benoit Gauzens, Kinlan Mehdi Goulwen Jan, and Monika Winder 2023***

**Contact:** Andreas Novotny, [mail\@andreasnovotny.se](mailto:mail@andreasnovotny.se)

[![](https://zenodo.org/badge/DOI/10.5281/zenodo.7545864.svg)](https://doi.org/10.5281/zenodo.7545864)

## Abstract

Models that estimate rates of energy flow in complex food webs often fail to account for species-specific prey selectivity of diverse consumer guilds. While DNA metabarcoding is increasingly used for dietary studies, its application for food web modeling has been limited due to methodological biases. Here we used data from dietary metabarcoding studies of zooplankton to calculate prey selectivity indices and assess energy fluxes in a pelagic resource-consumer network. We show that food web dynamics are influenced by species prey selectivity and temporal match-mismatch in growth cycles and that cyanobacteria are the main source of primary production in the investigated coastal pelagic food web. The latter challenges the common assumption that cyanobacteria are not supporting food web productivity, a result that is increasingly relevant as global warming promotes cyanobacteria dominance. While this is the first time that DNA metabarcoding is used to quantify energy fluxes in a food web model, the approach presented here can easily be extended to other ecosystems.

## Introduction

This directory contains the code and the data sets needed to set up the model, and reproduce the results and figures of the manuscript. Vignette_and_Analysis.Rmd guide the data filtration, model setup, and the creation of figures.\
\
All data needed for the analysis is found under /Data. Figures and tables will be saved in /Outputs and named after their manuscript counterparts.

## Datasets

The following data sets are found in the /Data directory:

### 16SrRNA_zp.rds

Contains annotated DNA sequences of zooplankton and water samples. The dataframe data frameollowing columns:

**OTU** DNA sequence identified by Illumina sequencing and DADA2 inference.\
**Sample** Unique zooplankton or water sample ID\
**SORTED_genus** Microscopically identified genus of pooled zooplankton individuals. Alternatively *Water* for water samples.\
**SAMPLE_date** Date of environmental sampling.\
**Domain** Assigned clade of OTU sequence in the SILVA database.\
**Supergroup** Assigned clade of OTU sequence in the SILVA database.\
**Phylum** Assigned clade of OTU sequence in the SILVA database.\
**Class** Assigned clade of OTU sequence in the SILVA database.\
**Order** Assigned clade of OTU sequence in the SILVA database.\
**Family** Assigned clade of OTU sequence in the SILVA database.\
**Genus** Assigned clade of OTU sequence in the SILVA database.\
**Species** Assigned clade of OTU sequence in the SILVA database.\
**STATION_ID** Id of sampling location\
**Abundance** Relative read abundance of OTU, relative to all OTUs per Sample

### Phytoplankton_shark.rds

Phytoplankton observations downloaded from <https://sharkweb.smhi.se/hamta-data/>. See the database for metadata description.

### Zooplankton_shark.rds

Zooplankton observations downloaded from <https://sharkweb.smhi.se/hamta-data/>. See the database for metadata description.

### Temperatures.rds

Temperature observations downloaded from <https://sharkweb.smhi.se/hamta-data/>. See the database for metadata description.

### full_model_iteration.rds

Contains the major model output, and can be recreated in the Vignette.

## Dependencies

The model has been tested with the following dependencies:

R version 4.2.1 (2022-06-23 Platform: x86_64-apple-darwin17.0 (64-bit) Running under: macOS Monterey 12.6.1

attached base packages: stats graphics grDevices utils datasets methods base

other attached packages: lubridate_1.8.0 circlize_0.4.15 svglite_2.1.0 igraph_1.3.5 xts_0.12.2 zoo_1.8-11 forcats_0.5.2 stringr_1.4.1 dplyr_1.0.10 purrr_0.3.5 readr_2.1.3 tidyr_1.2.1 tibble_3.1.8 ggplot2_3.3.6 tidyverse_1.3.2

loaded via a namespace (and not attached): lattice_0.20-45 assertthat_0.2.1 digest_0.6.29 utf8_1.2.2 R6_2.5.1 cellranger_1.1.0 backports_1.4.1 reprex_2.0.2 evaluate_0.17 httr_1.4.4 pillar_1.8.1 GlobalOptions_0.1.2 rlang_1.0.6 googlesheets4_1.0.1readxl_1.4.1 rstudioapi_0.14 jquerylib_0.1.4 car_3.1-0 rmarkdown_2.17 googledrive_2.0.0 munsell_0.5.0 broom_1.0.1 compiler_4.2.1 modelr_0.1.9 xfun_0.33 systemfonts_1.0.4 pkgconfig_2.0.3 shape_1.4.6 htmltools_0.5.3 tidyselect_1.2.0 fansi_1.0.3 crayon_1.5.2 tzdb_0.3.0 dbplyr_2.2.1 withr_2.5.0 ggpubr_0.4.0 grid_4.2.1 jsonlite_1.8.2 gtable_0.3.1 lifecycle_1.0.3 DBI_1.1.3 magrittr_2.0.3 scales_1.2.1 cachem_1.0.6 cli_3.4.1 stringi_1.7.8 carData_3.0-5 ggsignif_0.6.4 fs_1.5.2 bslib_0.4.0 xml2_1.3.3 ellipsis_0.3.2 generics_0.1.3 vctrs_0.4.2 tools_4.2.1 glue_1.6.2 hms_1.1.2 abind_1.4-5 fastmap_1.1.0 yaml_2.3.5 colorspace_2.0-3 gargle_1.2.1 rstatix_0.7.0 rvest_1.0.3 knitr_1.40 haven_2.5.1 sass_0.4.2
