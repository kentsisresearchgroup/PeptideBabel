# PeptideBabel
Python script for generation of novel bioactive peptide sequences using Metropolis-Hastings sampling
#Overview
This algorithm generates novel peptides by exploring the sequence space around known and predicted penetration domains (or other bioactive sequences), using Markov chain Monte Carlo sampling (Metropolis-Hastings) with permutation of seed sequences mapped to a density function based on physicochemical features. This allows efficient generation of hundreds to millions of peptide sequences for subsequent empiric validation, tailored to application based on input peptides. Our initial implementation of this algorithm was to generate lists of potential cell-penetration peptides.
# Manifest
NoteBooks: 

library-design-2-with-physicochemical-density-estimation.ipynb - Jupyter notebook with most current PeptideBabel script

peptide properties master table generator.ipynb – Jupyter notebook with script to calculate peptide properties

k-mers.ipynb - Generates unique k-mers from seed library

k-mer-kernel baseline.ipynb -Jupyter notebook with alternative version of PeptideBabel, using k-mer features alone, without the physiochemical properties

Data: 

CPPsitelist.xls – sample seed library of known cell penetration domains, from CPPsite 2.0 (http://crdd.osdd.net/raghava/cppsite/)

# Dependencies

matplotlib

numpy

scipy

sci-kitlearn

pandas

biopython

tqdm (progress bars)

xlrd

lxml

pyteomics (preferred way to install is pip Python package manager)

# Usage

1.	Load reference peptides for seed library

•	Default: CPP library. Path_to_spreadsheet = ‘CPPsitelist.xlsx’

2.	Analysis of properties of the reference set:

•	Imports protein analysis tools

•	Some sections in progress to look at more nuanced peptide properties

3.	Define physicochemically-based distance metric 

•	Outputs principal component analyses

•	Isoelectric point and hydrophobicity are most prominent features

4.	Plots physicochemical distance metrics

5.	Estimate density in feature projection

6.	Design peptide libraries by sampling

•	Implements a random-walk Metropolis-Hastings

•	Analyses of output peptides and correlation times included 

# Authors

Josh Fass | josh.fass@choderalab.org

Nicole McNeer | mcneern@mskcc.org

Alex Kentsis | kentsisresearchgroup@gmail.com

John Chodera | john.chodera@choderalab.org
