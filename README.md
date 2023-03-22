# forager-analyses
This repository contains the analysis scripts for processing the data from the [forager](https://github.com/thelexiconlab/forager) package. 

## data

The `data` folder contains the data files returned by the forager package for a given fluency list. For a given fluency list, the data folder contains the following files:

* `..._individualitemfits.csv`: Item-wise lexical metrics (semantic similarity, phonological similarity, and word frequency) as well as the item-wise negative log-likelihoods (NLLs) for each chosen model and switch method
* `..._switchresults.csv`: The switch designations for each item for each selected switch method
* `..._modelresults.csv`: The model results with the optimal parameter values and NLL for each model and switch method run

We analyze forager outputs from two datasets (`psyrev_data.txt` and `sz_data.txt`), both of which are available in their respective subfolders (`data/psyrev_data` and `data/sz_data`) inside the `data` folder. Users are encouraged to read the following papers for more details about the datasets:

- `psyrev_data`: Hills, T. T, Jones, M. N, & Todd, P. M (2012). Optimal foraging in semantic memory. *Psychological Review*, *119*(2), 431–440.
- `sz_data`: Lundin, N. B., Todd, P. M., Jones, M. N., Avery, J. E., O’Donnell, B. F., & Hetrick, W. P. (2020). Semantic search in psychosis: Modeling local exploitation and global exploration. *Schizophrenia Bulletin Open*, *1*(1), sgaa011.

## scripts

The `.Rmd` file contains the code for analyzing the data from the forager package. The `.html` file contains the output of the .Rmd file.

### psyrev data

For the psyrev data (inside `data/psyrev_data`), we analyze the data in two ways:

* We examine the cluster/switch predictions for a given participant (51) for demonstration purposes.
* We examine the sum of negative log-likelihoods (NLLs) for each model and switch method for all participants to determine the best model and switch method.

### sz data

For the sz data (inside `data/sz_data`), we analyze the data in three ways:

* Number of items: We examine the number of items produced by participants across the three diagnostic groups (healthy controls, schizophrenia group, schizotypal group).
* Cluster size and switches: We examine the mean cluster size and number of switches for each diagnostic group.
* Parameter values: We examine the parameter values (betas) for the different lexical sources (semantic similarity and frequency) for each diagnostic group for the dynamic foraging model fit with the similarity drop method for cluster/switch designations.



