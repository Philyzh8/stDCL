# stDCL

[![PyPI - Python Version](https://img.shields.io/pypi/pyversions/stDCL)(https://pypi.org/project/stDCL/)]
[![License](https://img.shields.io/badge/License-MIT-green.svg)](https://opensource.org/licenses/MIT)
[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.10968451.svg)](https://zenodo.org/records/10968451)

`stDCL` is a Python package containing tools for identifing spatial domains from spatial transcriptomics data based on a dual graph contrastive learning method.

- [Overview](#overview)
- [System Requirements](#system-requirements)
- [Installation Guide](#installation-guide)
- [Usage](#Usage)
- [Data Availability](#data-availability)
- [License](#license)


# Overview
Recent advances in spatial transcriptomics have enabled simultaneous preservation of high-throughput gene expression profiles and spatial context, enabling the high-resolution exploration of distinct regional characterization in brain tissue. However, the complex spatial structure of brain poses challenges in capturing spatial heterogeneity effectively and deciphering internal regulatory mechanisms accurately. Here, we develop stDCL, a dual graph contrastive learning method to identify spatial domains from spatial transcriptomics data. stDCL adaptively incorporates gene expression data and spatial information via a graph embedding autoencoder, thereby preserving critical information within latent embedding representations. Then, we propose dual graph contrastive learning to train the model, ensuring that the latent embedding representation closely resembles the actual spatial distribution and exhibits cluster similarity. Benchmarking stDCL against other state-of-the-art clustering methods using cerebral cortex datasets demonstrates its superior accuracy and effectiveness in identifying spatial domains. Our analysis of the imputation matrices generated by stDCL reveals its capability to reconstruct spatial hierarchical structures and refine differential expression assessments. Furthermore, we illustrate the central role of stDCL in elucidating gene regulation, spatial heterogeneity, and developmental patterns in the brain. Additionally, stDCL can also be instrumental in annotating disease-associated cellular phenotypes in Alzheimer's disease, unraveling the regulatory mechanisms.


![1811713010487_ pic](https://github.com/Philyzh8/stDCL/assets/65069252/f15928c1-59c2-4936-82f2-be39a3426456)

# System Requirements
## Hardware requirements
`stDCL` package requires only a standard computer with enough RAM to support the in-memory operations.

## Software requirements
### OS Requirements
This package is supported for *Linux*. The package has been tested on the following systems:
+ Linux: Ubuntu 18.04

### Python Dependencies
`stDCL` mainly depends on the Python scientific stack.
```
numpy
scipy
torch
scikit-learn
pandas
scanpy
```
For specific setting, please see <a href="https://github.com/Philyzh8/stDCL/blob/master/requirements.txt">requirement</a>.

# Installation Guide:

### Install from PyPi

```
$ conda create -n stDCL_env python=3.8.15
$ conda activate stDCL_env
$ pip install -r requirements.txt
$ pip install stDCL
```

# Usage
`stDCL` is a dual graph contrastive learning method for identifing spatial domains, which can be used to:
+ Single-cell data clustering. The example can be seen in the <a href="https://github.com/Philyzh8/scMGCA/blob/master/tutorial/demo.py">demo.py</a>.
+ Correct the batch effect of data from different scRNA-seq protocols. The example can be seen in the <a href="https://github.com/Philyzh8/scMGCA/blob/master/tutorial/demo_batch.py">demo_batch.py</a>.
+ Analysis of the mouse brain data with 1.3 million cells. The example can be seen in the <a href="https://github.com/Philyzh8/scMGCA/blob/master/tutorial/demo_scale.py">demo_scale.py</a>.
+ Provide an automatic hyperparameter search algorithm. The example can be seen in the <a href="https://github.com/Philyzh8/scMGCA/blob/master/tutorial/demo_para.py">demo_para.py</a>.

We give users some suggestions for running in the <a href="https://github.com/Philyzh8/scMGCA/blob/master/tutorial/tutorial.md">tutorial.md</a>.


# Data Availability

The real data sets we used can be download in <a href="https://zenodo.org/records/10968451">data</a>.

# License

This project is covered under the **MIT License**.


