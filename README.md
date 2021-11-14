# Grouping-countries-based-on-socio-economic-factors-for-NGO-aid.
The problem statement here is to cluster the countries based on certain socio-economic and health  factors to identify countries that are in dire need of aids.  
This projects was done in following steps:

EDA: We read the data, check for missing or inappropriate values, wrong data formats. The data set  requires no cleaning.Perform Univariate and Bivariate analysis and different kinds of visualization. This  can help us choose the variables required for Clustering. 

Feature selection, Outlier analysis, scaling the data, Hopkin’s test for Clusterability : After performing  EDA we decide to select the columns “gdpp”,”child_mort” and “income” as the variables for clustering  model. We observe from the box plot that outliers do exist but looking at the data we notice that the  outliers actually make sense since there are countries that are developed, have high income and better  healthcare and some countries are extremely poverty struck. It would be biased to remove these values  from the analysis. Standardscaler is used to standardize the variables. The Hopkin’s statistic test value is  about 0.856 which indicates the data is clusterable.  

SSD/ elbow curve and Silhouette analysis to determine optimal number of clusters: According to SSD and  Silhouette 4 clusters are optimal but upon observation we find 3 clusters as ideal i.e. developed, under  developed and developing country.  

K means Clustering Model: With 3 clusters (0: developed, 1: developing, 2: under developed) 

Hierarchical Clustering with single linkage and complete linkage: Complete linkage provides better  clusters hence we retain complete linkage model. 

Comparison of K means and Hierarchical Clustering and visualising: Hierarchical clustering is biased  towards developing countries whereas K means provides better clustering. Hence we proceed with the  K-means to list the countries that require aids. Which are the countries with low gdpp, high child_mort  and low income. 

Extracting countries in need of aid: The countries of cluster – under developed are the countries that  require aid. Some of them are Burundi, Liberia, Congo, Dem. Rep., Niger and Sierra Leone.
