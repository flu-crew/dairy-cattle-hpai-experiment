# Dairy cows inoculated with highly pathogenic avian influenza virus H5N1  
[![DOI](https://zenodo.org/badge/835369959.svg)](https://zenodo.org/doi/10.5281/zenodo.13126628)

This repository will host scripts and describe how to reproduce the computational analysis in:

*Baker, et al. **Dairy cows inoculated with highly pathogenic avian influenza virus H5N1**. Nature (2024) [DOI and link to early release article](https://doi.org/10.1038/s41586-024-08166-6)*

If you have queries on material in this repo, please create an issue and it will be addressed.

### Raw read data from the study ###
Raw read data generated during this study are archived at USDA National Agricultural Library - AgDataCommons and may be accessed (pending releaase 11/12/2024) at the following:

Baker AL, Arruda B, Palmer MV, Boggiatto P, Davila KS, Buckley A, Zanella GC, Snyder CA, Anderson TK, Hutter CR, Nguyen TQ, Markin, A, Lantz, K, Posey, EA, Torchetti, MK, Robbe-Austerman, S, Magstadt, DR, Gorden, PJ. (2024). Data from: Dairy cows inoculated with highly pathogenic avian influenza virus H5N1. AgDataCommons, https://doi.org/10.15482/USDA.ADC/27325716 

### Project structure ###
See the respective README.txt files within the folders for details/instructions.
- [ML_Trees](ML_Trees/): Input and output from the genetic sequence analysis: includes PDF tree figures and NCBI Genbank accessions of data from prior study that was used again in this work.
- [SNV_results](SNV_results/): Variant calling analysis. All tables and data generated from within-host variant calling analysis.
- [clinical-challenge-study-data.xlsx](): all supplemental tables and data associated with manuscript.
- [WGS-representativity](WGS-representativity/): Analysis to identify how representative the challenge strain was relative to field collected samples.
