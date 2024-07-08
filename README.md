<img src="thumbnail.png" alt="thumbnail" width="300"/>
<img src="https://github.com/LinkedEarth/Logos/blob/master/LinkedEarth_medium.png?raw=true" alt="LinkedEarth Logo" width="500">

# Investigating interhemispheric precipitation changes over the past millennium

[![nightly-build](https://github.com/ProjectPythia/paleoPCA-Cookbook/actions/workflows/nightly-build.yaml/badge.svg)](https://github.com/ProjectPythia/paleoPCA-Cookbook/actions/workflows/nightly-build.yaml)
[![Binder](https://binder.projectpythia.org/badge_logo.svg)](https://binder.projectpythia.org/v2/gh/ProjectPythia/paleoPCA-Cookbook/main?labpath=notebooks)
[![DOI](https://zenodo.org/badge/813352705.svg)](https://zenodo.org/badge/latestdoi/813352705)

This Project Pythia Cookbook covers paleoclimate model-data comparison using spatio-temporal pattern obtained using Principal Component Analysis (PCA).

## Motivation

Paleoclimate observations obtained from tree rings or the geochemical composition of speleothems, ice and sediments provide an out-of-sample validation of climate models. However, comparing the output of climate models directly with the paleoclimate observations is difficult: (1) they are often expressed in different quantities (i.e., temperature vs ring width), (2) paleoclimate observations have large time uncertainties, (3) paleoclimate observations often incorporate more than one environmental signal (i.e., temperature AND moisture).

Recently, [Steinman et al. (2022)](https://doi.org/10.1073/pnas.2120015119) used PCA analysis to compare model and data output. Here, we use a similar approach with the [CESM Last Millennium simulation](https://www2.cesm.ucar.edu/models/cesm1.2/) and proxy records stored on the [LiPDverse](https://lipdverse.org). This repository contains paleoclimate datasets that have been curated by the community and are archived in a standard format, facilitating analysis. 

## Authors

[Deborah Khider](https://github.com/khider), [Hari Sundar](https://github.com/sriharisundar), [Varun Ratnakar](https://github.com/varunratnakar)

### Contributors

<a href="https://github.com/ProjectPythia/paleoPCA-Cookbook/graphs/contributors">
  <img src="https://contrib.rocks/image?repo=ProjectPythia/paleoPCA-Cookbook" />
</a>

## Structure

This Cookbook is broken down into three main sections. The first section performs the PCA analysis on the output of the CESM LME simulation. The second section performs the same analysis on paleoclimate observations. The last section compares the two analyses.

### PCA analysis on proxy observations

The section shows the query used to obtain relevant proxy datasets from a graphDB mirroring the LiPDverse data, filtering for records that cover at least 1500 of the last 2000 years with a resolution better than 60 years, and running PCA.

### PCA analysis on the CESM Last Millennium Analysis¶

The section walks through fetching the data from JetStream2, calculating the precipitation d18O and running PCA. 


### Model Data Comparison

Visualizing the output of the PCA analyses. 

## Running the Notebooks

You can either run the notebook using [Binder](https://binder.projectpythia.org/) or on your local machine.

### Running on Binder

The simplest way to interact with a Jupyter Notebook is through
[Binder](https://binder.projectpythia.org/), which enables the execution of a
[Jupyter Book](https://jupyterbook.org) in the cloud. The details of how this works are not
important for now. All you need to know is how to launch a Pythia
Cookbooks chapter via Binder. Simply navigate your mouse to
the top right corner of the book chapter you are viewing and click
on the rocket ship icon, (see figure below), and be sure to select
“launch Binder”. After a moment you should be presented with a
notebook that you can interact with. I.e. you’ll be able to execute
and even change the example programs. You’ll see that the code cells
have no output at first, until you execute them by pressing
{kbd}`Shift`\+{kbd}`Enter`. Complete details on how to interact with
a live Jupyter notebook are described in [Getting Started with
Jupyter](https://foundations.projectpythia.org/foundations/getting-started-jupyter.html).

### Running on Your Own Machine

If you are interested in running this material locally on your computer, you will need to follow this workflow:

1. Clone the `https://github.com/ProjectPythia/paleoPCA-Cookbook` repository:

   ```bash
    git clone https://github.com/ProjectPythia/paleoPCA-Cookbook.git
   ```

1. Move into the `paleoPCA-Cookbook` directory
   ```bash
   cd paleoPCA-Cookbook
   ```
1. Create and activate your conda environment from the `environment.yml` file
   ```bash
   conda env create -f environment.yml
   conda activate paleoPCA-Cookbook
   ```
1. Move into the `notebooks` directory and start up Jupyterlab
   ```bash
   cd notebooks/
   jupyter lab
   ```
