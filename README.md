# Bushhouse_Riboswitch_Sensitivity_2024
Code for Bushhouse et al. "RNA folding kinetics control riboswitch sensitivity in vivo"

## Contents

This repo contains four Jupyter notebooks used to perform data analysis for Bushhouse et al. "RNA folding kinetics control riboswitch sensitivity in vivo".

1. `Supp_Code_File_Hill-Fitting.ipynb` contains scripts to perform dose response fitting on the fluorescence data provided in Supplementary Data File 1.
2. `Supp_Code_File_Bioinformatics.ipynb` contains an analysis pipeline used to capture ZTP riboswitch expression platforms based on putative aptamer domains identified in [Rfam](https://rfam.org/family/RF01750). This notebook requires `RF01750.csv` as an input.
3. `Supp_Code_File_FACS-seq_1.ipynb` contains the first half of a data analysis pipeline to process FACS-seq data for ZTP riboswitch terminator loop variants. This portion of the pipeline processes sequencing data and estimates mean fluorescence for each loop variant in each ligand condition. Sequencing data for this experiment is available in [SRA](https://www.ncbi.nlm.nih.gov/sra/?term=PRJNA1087340). Metadata files `Rep1_CellCounts.txt` and `Rep2_CellCounts.txt` are required inputs.
4. `Supp_Code_File_FACS-seq_2.ipynb` contains the second half of a data analysis pipeline to process FACS-seq data for ZTP riboswitch terminator loop variants. This portion of the pipeline pools data from both experimental replicates to fit dose response data to the Hill function, extract functional parameters, and generate a functional landscape plot.

## System requirements

To run this code a Python 3 Jupyter notebook environment must be prepared with the following packages installed in addition to the standard library:

```
biopython
pandas
numpy
ViennaRNA
scipy
scikit-learn
matplotlib
```

There should be no OS requirements. The code has been tested on machines with conda python environments running MacOS 14.

## Installation Guide

Clone repo contents from Github (should take a few seconds):
```
git clone https://github.com/LucksLab/Bushhouse_Riboswitch_Sensitivity_2024
```

Open using Jupyter Notebook in an environment satisfying above requirements.

## Demo Data for Fitting Code

`Supp_Code_File_Hill-Fitting.ipynb` can be tested on the demo data provided in `DEMO.xlsx`. This should produce an output `.csv` with an EC50 calculation of 116.4279 μM. This should take less than a second.