# SDSE_transmission

Code used to generate transmission networks and models for SDSE/S. pyogenes transmission manuscript (https://doi.org/10.1101/2023.08.17.23294027).

Partial metadata is provided here to allow replication of analysis while protecting participant confidentiality.
Scripts are provided as R markdown files which can be knitted as provided to generate manuscript results.

Tested on a M1 Mac system with:
- R v4.3.1
- tidyverse v2.0.0
- igraph v1.5.1
- gridExtra v2.3
- ggplot2 v3.4.3
- plotfunctions v1.4
- ggraph v2.1.0
- tidygraph v1.3.0
- scatterpie v0.2.1
- lubridate v1.9.3

Example scripts should run in ~2 minutes on a standard laptop.

## Scripts
1) **sdse_transmission_networks_comm_1.Rmd** <br>
Generates transmission networks for SDSE and S. pyogenes for community **1**. Also implements the node permutation model to simulate a model of indepedent transmission.
2) **sdse_transmission_networks_comm_3.Rmd*** <br>
Generates transmission networks for SDSE and S. pyogenes for community **3**. Also implements the node permutation model to simulate a model of indepedent transmission.
3) **co_occurrence.Rmd** <br>
Calculates number of household-visits where SDSE and S. pyogenes are observed in the same household. Implements as model of independent inter and intra-species transmission by permuting positive swabs across all swabs taken in a community visit while accounting for clustering of isolates from the same genomic transmission cluster within household-visits.

## Data
1) **sdse_clusters_comm_1.csv** <br>
Transmission clusters for SDSE isolates from community 1
2) **sdse_clusters_comm_3.csv** <br>
Transmission clusters for SDSE isolates from community 3
3) **pyo_clusters_comm_1.csv** <br>
Transmission clusters for S. pyogenes isolates from community 1
4) **pyo_clusters_comm_3.csv** <br>
Transmission clusters for S. pyogenes isolates from community 3
5) **HHsize_community_combined.csv** <br>
Household size from both communities. Household sizes were inferred by the number of unique individuals sampled at each household over the study period.
6) **HH_prop_comm_1.csv** <br>
Proportion of SDSE and S. pyogenes from all positive swabs in households in community 1
7) **HH_prop_comm_3.csv** <br>
Proportion of SDSE and S. pyogenes from all positive swabs in households in community 3
8) **co_occur_df.csv** <br>
All episodes where an individual was sampled. Each episode may be associated with more than one swab (e.g., throat and one or more skin swabs)
9) **all_pos_df.csv** <br>
All positive swabs including those which were not available for sequencing.
10) **sdse_metadata.csv** <br>
Abbreviated metadata table from manuscript Supplementary Table 1.
11) **pyo_metadata.csv** <br>
Abbreviated metadata table from Lacey et al. DOI: 10.1016/s2666-5247(23)00068-x
12) **sampling_intervals.csv** <br>
Dates of community visits
