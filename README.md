## Ballycanew_Ptool

A repository to analyze the results of the BBN development and parametrization in the Ballycanew catchment. This is a repository for the paper titled "Bayesian network modelling of phosphorus pollution in agricultural catchments with high-resolution data".

# Code
There area several R files aimed at the analysis of the BBN developed in this study:

- DischargeDistributions.Rmd - a file detailing the bootstrapping procedure aimed at obtaining monthly discharge distributions for the BBN.

- TurbidityDistributions.Rmd - a file detailing the bootstrapping procedure aimed at obtaining monthly turbidity distributions for the BBN.

- Genie_Results.Rmd - a file detailing the code used for the analysis of the BBN results.

- figures_for_publication.Rmd - a file detailing the code used to obtain the figures used in the publication.

- ObservedMonthlyP.Rmd - a file detailing the bootstrapping procedure aimed at obtaining monthly TRP distributions for the BBN.

# Data and Results
There is a data folder containing:
- the original datasets (Ballycanew_data.csv - daily TRP concentrations, Ballycanew_discharge.csv - daily total discharge, Ballycanew_Turbidity_Sediments. csv - daily turbidity and sediment concentrations)

- the csv files of the distributions obtained from bootstrapping the original datasets (monthly_fitted_TRP_observations.csv, monthly_fitted_Q_observations_Ballycanew.csv, monthly_turbidity_distributions_Ballycanew.csv, monthly_discharge_distributions.csv)

- the two models files (Model A in DiffusePtool_v4.xdsl and Model B in Ptool_pointanddiffuse_v4.xdsl)

There is a results folder containing:
- The results of the two BBNs (20230920_Ptool_v4.csv, 20230920_Ptool_v4_months.csv, 20230920_DiffusePtool_v4.csv, 20230920_DiffusePtool_v4_months.csv)

- The results of Genie_Results.Rmd (20230920_filtered_DiffusePtool_v4_monthly_means.csv, 20230920_filtered_DiffusePtool_v4_monthly_median.csv, 20230920_filtered_Ptool_v4_monthly_means.csv, 20230920_filtered_Ptool_v4_monthly_median.csv)

- The figure files made with the figures_for_publication.Rmd file. 

Spatial datasets are not part of this repository, but the paper reports summary information on them as well as references to their original research.
