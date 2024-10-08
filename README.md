# Ballycanew_Ptool

A repository to analyze the results of the BBN development and parametrization in the Ballycanew catchment. This is a repository for the paper titled "Bayesian network modelling of phosphorus pollution in agricultural catchments with high-resolution data".

## Start here

Two Bayesian Belief Networks for phosphorus losses in an Irish agricultural catchment are parametrized and analyzed here. The BBNs were developed with the GeNIe tool (free for academics, https://download.bayesfusion.com/files.html?category=Academia) and can be accessed at these two files: DiffusePtool_v4.xdsl, Ptool_pointanddiffuse_v4.xdsl in the data folder [Go to Data and Results section](#data-and-results). This model was developed with Genie version 2.4. To simulate P losses at the stream outlet, open a BBN file and hit the lightning button. The posterior distributions can be visualized when opening the "In stream TRP concentration mg L-1" node, clicking on the "value" tab. These can be copied and pasted onto a csv file. The R code in GenieResults.Rmd is set up to analyzed results from both BBNs as is and with posterior distributions of TRP concentration per month (this is obtained by selecting each month as evidence prior to triggering the model with the lightning button. Posterior distributions of "In stream TRP concentration mg L-1" are already uploaded in the [results folder](https://github.com/CamillaNegri/Ballycanew_Ptool/tree/main/results)) . 
In the [Code section](#code)  you can find a description of all the Rmd files for the both the BBN paramtetrization and the analysis of results. 

## Code

There are several R files aimed at the analysis of the BBN developed in this study:

- [DischargeDistributions.Rmd](https://github.com/CamillaNegri/Ballycanew_Ptool/blob/main/DischargeDistributions.Rmd) - a file detailing the bootstrapping procedure to obtain monthly discharge distributions for the BBN.

- [TurbidityDistributions.Rmd](https://github.com/CamillaNegri/Ballycanew_Ptool/blob/main/TurbidityDistributions.Rmd) - a file detailing the bootstrapping procedure to obtain monthly turbidity distributions for the BBN.

- [GenieResults.Rmd](https://github.com/CamillaNegri/Ballycanew_Ptool/blob/main/GenieResults.Rmd) - a file detailing the code used for the analysis of the BBN results.

- [FiguresPublication.Rmd](https://github.com/CamillaNegri/Ballycanew_Ptool/blob/main/FiguresPublication.Rmd) - a file detailing the code used to obtain the figures used in the publication.

- [ObservedMonthlyP.Rmd](https://github.com/CamillaNegri/Ballycanew_Ptool/blob/main/ObservedMonthlyP.Rmd) - a file detailing the bootstrapping procedure to obtain monthly BBN Total Reactive Phosphorus(TRP) distributions from the observed TRP.

## Data and Results

There is a [data folder](https://github.com/CamillaNegri/Ballycanew_Ptool/tree/main/data) containing:
- the original datasets (Ballycanew_data.csv - daily TRP concentrations, Ballycanew_discharge.csv - daily total discharge, Ballycanew_Turbidity_Sediments. csv - daily turbidity and sediment concentrations)

- the csv files of the distributions obtained from bootstrapping the original datasets (monthly_fitted_TRP_observations.csv, monthly_fitted_Q_observations_Ballycanew.csv, monthly_turbidity_distributions_Ballycanew.csv, monthly_discharge_distributions.csv). The models do not use the full distributions of discharge and turbidity obtained here but rather the distributions parameters are used in GeNIe to generate the distributions. The generated TRP distributions are used for the results analysis. 

- the two models files (Model A in [DiffusePtool_v4.xdsl](https://github.com/CamillaNegri/Ballycanew_Ptool/blob/main/data/DiffusePtool_v4.xdsl) and Model B in [Ptool_pointanddiffuse_v4.xdsl](https://github.com/CamillaNegri/Ballycanew_Ptool/blob/main/data/Ptool_pointanddiffuse_v4.xdsl)

There is a [results folder](https://github.com/CamillaNegri/Ballycanew_Ptool/tree/main/results) containing:
- The results of the two BBNs (20230920_Ptool_v4.csv, 20230920_Ptool_v4_months.csv, 20230920_DiffusePtool_v4.csv, 20230920_DiffusePtool_v4_months.csv) generated within GeNIe.

- The results of the analysis of the posterior distributions carried out in the [GenieResults.Rmd](https://github.com/CamillaNegri/Ballycanew_Ptool/blob/main/GenieResults.Rmd) code, and saved as csv files (20230920_filtered_DiffusePtool_v4_monthly_means.csv, 20230920_filtered_DiffusePtool_v4_monthly_median.csv, 20230920_filtered_Ptool_v4_monthly_means.csv, 20230920_filtered_Ptool_v4_monthly_median.csv)

- The figure files which are made with the [FiguresPublication.Rmd](https://github.com/CamillaNegri/Ballycanew_Ptool/blob/main/FiguresPublication.Rmd) file

Spatial datasets are not part of this repository, but the paper reports summary information on them as well as references to research that originated them.

## Open Access peer-reviewed article
Camilla Negri, Per-Erik Mellander, Nicholas Schurch, Andrew J. Wade, Zisis Gagkas, Douglas H. Wardell-Johnson, Kerr Adams, Miriam Glendell,
Bayesian network modelling of phosphorus pollution in agricultural catchments with high-resolution data,
Environmental Modelling & Software, Volume 178, 2024, 106073, ISSN 1364-8152, https://doi.org/10.1016/j.envsoft.2024.106073.

## Preprint
https://doi.org/10.31223/X5KX2R

## Acknowledgments

![Agricultural Catchments Programme logo](https://github.com/CamillaNegri/Ballycanew_Ptool/blob/main/Acknowledgments/ACP-logo.png)
![Teagasc- Agriculture and Food Development Authority logo](https://github.com/CamillaNegri/Ballycanew_Ptool/blob/main/Acknowledgments/logo-teagasc2x.png)
![University of Reading logo](https://github.com/CamillaNegri/Ballycanew_Ptool/blob/main/Acknowledgments/UoR_logo.png)
![The James Hutton Institute logo](https://github.com/CamillaNegri/Ballycanew_Ptool/blob/main/Acknowledgments/JHI_logo.jpg)
![Biomathemathics and Statistics Scotland (BioSS) logo](https://github.com/CamillaNegri/Ballycanew_Ptool/blob/main/Acknowledgments/BioSS_logo.png)


