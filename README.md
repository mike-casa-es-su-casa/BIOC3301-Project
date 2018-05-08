# Archaea in Gordon Square Park Soil :leaves:
## A summary of scripts used to identify any possible relationship phylums within the Archaea kingdom may have based on soil nutrient concentrations, pH and vegetation presence. 

#### Core Microbiome 

The core microbiome, taxa found in 98% of samples, was computed using 
> compute_core_microbiome.py -i ~/2018_02_smb/OTU18/otu_table.biom -o 98_core_otu.biom --min_fraction_for_core 0.98 

And the following 11 phyla were identified. Only one, *Crenarchaeota*, is in the Archaea kingdom.

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

#### Core Diversity Analysis

The Core Diversity Analysis runs a series of tests for alpha and beta diversity. It also plots a bar chart of the relative abundance of each phylum in each soil sample.This script was used after filtering out 2017 samples and samples out of Gordon Square Park:

> core_diversity_analyses.py 

The same data was used to plot a heatmap to show the relative abundance of each species spread across samples. 

> make_otu_heatmap.py 

### Statistical Tests

The following scripts were used to calculate correlations in continous data and categorical data. The results for them are found in the directory [Core_Study_Stats](https://github.com/mike-casa-es-su-casa/BIOC3301-Project/tree/master/core_study_stats).

> observation_metadata_correlation.py
and
> group_significance.py
