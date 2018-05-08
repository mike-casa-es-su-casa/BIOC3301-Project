# Archaea in Gordon Square Park Soil :leaves:
## A summary of scripts used to identify any possible relationship phylums within the Archaea kingdom may have based on soil nutrient concentrations, pH and vegetation presence. 

### Core Microbiome 

The core microbiome, taxa found in 98% of samples, was computed using:

> compute_core_microbiome.py

And the following 11 phyla were identified. Only one, *Crenarchaeota*, is in the Archaea kingdom

* Crenarchaeota
* Acidobacteria
* Actinobacteria
* Bacteroidetes
* Chloroflexi
* Firmicutes
* Gemmatimonadetes
* Nitrospirae
* Planctomycetes
* Proteobacteria
* Verrucomicrobia

### Core Diversity Analysis

The Core Diversity Analysis runs a series of tests for alpha and beta diversity. It also plots a bar chart of the relative abundance of each phylum in each soil sample.This script was used after filtering out 2017 samples and samples out of Gordon Square Park:

> core_diversity_analyses.py 

The Level 2 (phylum) taxa summary shows the relative abundance for each sample

![L2 Taxa Summary](/CDA/taxa_plots/taxa_summary_plots/charts/DZ7y4rN6BJRh0XjhwmxQkF1phz5zkz.png)


The same data was used to plot a heatmap to show the relative abundance of each species spread across samples. 

> make_otu_heatmap.py 

![Heat Map](/heatmap)


### Statistical Tests

The following scripts were used to calculate correlations in continous data and significant abundances in categorical data. 

> observation_metadata_correlation.py

and 

> group_significance.py

The results for correlation against nutrients and pH is found [here](https://github.com/mike-casa-es-su-casa/BIOC3301-Project/tree/master/core_study_stats/correlate)

The results for significant abundance is found [here](https://github.com/mike-casa-es-su-casa/BIOC3301-Project/tree/master/core_study_stats/groupsig)

Correlations are only identifable with continous data, the table below summarises the data conversion for this:

Categorical Data Value | Nitrogen(%) | Phosphorus (ppm) | Potassium (ppm)
------------ | ------------- | ------------- | -------------
Low | 0.05 | 15 | 150
Medium | 0.1 | 20 | 200 
High | 0.2 | 30 | 300

### Step by Step Script Guide

A summary of all the scripts used step by step can be found in the repository [step-by-step script](https://github.com/mike-casa-es-su-casa/BIOC3301-Project/blob/master/Step-by-Step%20Script)
