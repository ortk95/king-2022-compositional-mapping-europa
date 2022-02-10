# Compositional Mapping of Europa
Supplementary material for King et al. (2022):

*Compositional Mapping of Europa using MCMC Modelling of Near-IR VLT/SPHERE and Galileo/NIMS Observations*

Oliver King, Leigh Fletcher & Nicolas Ligier

[![DOI](https://zenodo.org/badge/456963954.svg)](https://zenodo.org/badge/latestdoi/456963954)


## Description
Files starting with `reflectance_` provide mapped spectral reflectance data for the VLT/SPHERE and Galileo/NIMS datasets used in this study.

Files starting with `fit_` provide mapped MCMC compositional fit results for the VLT/SPHERE and Galileo/NIMS datasets used in this study. The fit results contain the fitted best estimate abundances and 1-sigma upper and lower bound abundances calculated from the posterior abundance distribution for each endmember at each observed location.


## Data format
These files are saved as compressed (gzipped) [JSON](https://www.json.org) data files.

All major programming languages provide support for reading JSON files. The code snippet below shows an example of how to directly open and use these data files in Python:
```python
import json
import gzip

with gzip.open('fit_SPHERE.json.gz', 'r') as f:
    data = json.load(f)

print(data.keys()) # print structure of data file
print(data['description'])
```
