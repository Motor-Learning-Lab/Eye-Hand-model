# Eye-Hand-model
This repository contains the analysis code and result visualization code for two visuomotor rotation experiments investigating the effect of manipulations of visuomotor adaptation on eye movements (2-target and 8-target). The code is organized into four main Jupyter notebooks, each serving a specific purpose in the analysis pipeline.
## Environment Setup
To ensure compatibility and reproducibility, the required environment is provided in pymc5_env.yml. This file specifies all necessary dependencies, including libraries for Bayesian modeling, data processing, and visualization.
## Code Details
### EyeHand_preprocess.ipynb
This script is responsible for the data preprocessing phase. Here, we import hand movement data collected from PsychoPy and raw eye-tracking data to pre-process them to generate the key metrics necessary for further analysis.
  * Input: Raw hand data from PsychoPy (change the path <hand location>) and eye-tracker files (change the path <eye location>).
  * Output: A data table containing computed hand angles, eye angles, reaction times, etc.
  * The preprocessed tables are saved as .csv files and are subsequently imported by the Bayesian statistics notebooks.
### BayesianStatistics-2target.ipynb
This notebook performs Bayesian modeling on the 2-target experiment data. The table generated in EyeHand_preprocess.ipynb is loaded to fit a Bayesian model, capturing both the individual and group-level patterns of hand movements, eye movements, and reaction times.
* Key Outputs: Posterior distributions of model parameters, summaries of model fit results, and credible intervals.
### BayesianStatistics-8target.ipynb
Similar to the 2-target notebook, this notebook performs Bayesian analysis on the 8-target experiment data.
### Plot_figure_final.ipynb
This notebook visualizes the core results of the study.
## How to Run
1. Run the Preprocessing Script: Start with EyeHand_preprocess.ipynb to generate the preprocessed data tables.
2. Run Bayesian Analysis: Open and run BayesianStatistics-2target.ipynb and BayesianStatistics-8target.ipynb sequentially.
3. Generate Figures: Finally, execute Plot_figure_final.ipynb to create the visualizations for the paper.
