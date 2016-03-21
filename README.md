
[<img src="https://github.com/QuantLet/Styleguide-and-FAQ/blob/master/pictures/banner.png" width="880" alt="Visit QuantNet">](http://quantlet.de/index.php?p=info)

## [<img src="https://github.com/QuantLet/Styleguide-and-Validation-procedure/blob/master/pictures/qloqo.png" alt="Visit QuantNet">](http://quantlet.de/) **DataExpo2013_QuachSymanzikForsgren** [<img src="https://github.com/QuantLet/Styleguide-and-Validation-procedure/blob/master/pictures/QN2.png" width="60" alt="Visit QuantNet 2.0">](http://quantlet.de/d3/ia)

```yaml

Name of Quantlet : DataExpo2013_QuachSymanzikForsgren

Published in : Computational Statistics, Data Expo 2013 Special Issue, Volume 31, Issue 3, 2016

Description : 'This repository contains supplementary material for the paper "Soul of the
Community: An Attempt to Assess Attachment to a Community" to enable the reader to reproduce the
analysis.'

Keywords : 'Machine Learning, Statistical Learning, Data Mining, Predictive Analytics, Random
Forests, Archetypes, Knight Foundation'

See also : 'Other articles in Data Expo 2013 Special Issue, accessible at
https://github.com/COSTDataExpo2013'

Author : Anna Quach, Juergen Symanzik, Nicole Forsgren

Submitted : August 27, 2015

Datafile : 'knightfoundation2008sotcdata.por, knightfoundation2009sotcdata.por,
knightfoundation2010sotcdata.por'

Main function : Read_Me.R

-1 : 'archetype_convex_hull_2008.png -- Fig. 7: Graphical representation of the three archetype
solution for the year 2008. The three points labeled 1, 2, and 3 are the archetypes. Communities
are colored by the dominating group according to the three attachment status levels.'

-2 : 'percentile_profile_archetypes_2008.png -- Fig. 8: Graphical representation to aid with the
interpretation of the three archetype solution for the year 2008. The points represent the
percentile for each archetype for each variable as compared to the average response to each
community. See Table 4 in Appendix B for the meaning of each variable.'

```

![Picture1](archetype_convex_hull_2008.png)

![Picture2](percentile_profile_archetypes_2008.png)


```r
# Soul of the Community: An Attempt to Assess Attachment to a Community
# Anna Quach, Juergen Symanzik, and Nicole Forsgren
# 3/19/2015
# 
# To produce a pdf file of the manuscript follow these steps:
# 
# 1) Set your working directory to where all the R scripts are saved.
# 1) Run 01_data_cleaning.R first to produce the final data set which most of 
#    the scripts will depend on.
# 2) Run any of these scripts in any order to produce the figures in the 
#    manuscript:
#   
# 02_remove_cases_and_variables_heatmap.R
# 03_create_map_and_sample_size_chart.R
# 04_dotchart_top_3_variables.R
# 05_rf_all_communities.R ***Takes hours to run!!!
# 06_rf_and_pcp_gary.R
# 
# These two scripts don't need to be ran in order to produce the manuscript, but 
# the results were used to create some of the tables:
# 
# tune_parameters.R
# PCA_index_vars_derivation.R
# 
# *Note that there is no code made available to produces results for the 
# Archetypal Analysis section due to privacy reasons. The figures are provided 
# instead.
# 
# 3) Run Soul_of_the_Community.rnw in RStudio. Make sure this file is saved in 
# the same folder where the figures are produced.

source("01_data_cleaning.R")

source("02_remove_cases_and_variables_heatmap.R")

# Install the ggmap and maps packages
source("03_create_map_and_sample_size_chart.R")

# Install the ggplot2 and plyr packages
source("04_dotchart_top_3_variables.R")

# Install the randomForest, plyr, RColorBrewer, and ggplot2 packages
source("05_rf_all_communities.R") 

# Install the RColorBrewer, GGally, randomForest, plyr, and ggplot2 packages
source("06_rf_and_pcp_gary.R")

```
