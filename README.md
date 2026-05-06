# cross-systems-behavioral-analytics
End-to-end R workflow for analyzing cross-system behavioral data in mice using independent-group and repeated-measures experimental designs.

# Overview 

This project investigates whether pharmacological blockade of nicotinic receptor subtypes produces distinct anxiety-related behavioral effects across multiple behavioral systems.

Behavioral responses were evaluated in:

β4E61C and β2E61C mouse genotypes
Control and treatment groups (CTRL vs MPEG)
Elevated O-Maze and Open Field assays

The workflow integrates:

Cross-assay behavioral analytics
Repeated-measures comparisons
Correlation analysis across systems
Publication-ready visualizations

# Data and Methods

The dataset contains behavioral measurements collected from mice tested across anxiety-related assays. The same animals were evaluated in multiple systems, enabling within-subject comparisons.

Behavioral Metrics
Time spent in anxiogenic zones
Open-arm and center occupancy
Transition frequency
Locomotor activity
Time-binned behavioral summaries
Statistical Workflow

The analysis pipeline includes:

Data cleaning and preprocessing
Feature engineering of behavioral variables
Shapiro-Wilk normality testing
Welch t-tests and Wilcoxon rank-sum tests
Repeated-measures ANOVA
Post hoc pairwise comparisons
Pearson/Spearman correlation analysis
Automated visualization generation using ggplot2

The workflow is designed to handle:

Unequal sample sizes
Non-normal distributions
Cross-system repeated-measures datasets


# Running the analysis:

Requirements:
The workflow was developed in R using R Markdown and requires the following package -
library(tidyverse)
library(rstatix)
library(ggplot2)
library(emmeans)

Install missing packages with: 

install.packages(c(
  "tidyverse",
  "rstatix",
  "ggplot2",
  "emmeans"
))

Repository setup: Clone the repository

git clone https://github.com/yourusername/cross-systems-behavioral-analytics.git
cd cross-systems-behavioral-analytics 

Data Setup: 

Raw behavioral CSV files are not included in this repository.
Before running the analysis, update the data directory inside OmazeCODEgit.rmd - base_dir <- "path/to/your/local/data"

# Reproducibility

The workflow was designed as a reproducible behavioral analytics pipeline.
Because raw experimental datasets are not publicly distributed, users must
provide local copies of the behavioral CSV files before running the analysis.

# Example outputs:
Running the workflow generates:

Statistical summaries for O-Maze and Open Field assays
Group comparison tables and normality testing results
Cross-assay behavioral correlation analyses
Publication-ready behavioral visualizations
Exported CSV summaries and serialized R objects

Generated outputs are automatically written to:
outputs/plots/
outputs/tables/

Example outputs include:

O-Maze open-arm occupancy visualizations
Open Field locomotor and transition summaries
Cross-assay behavioral correlation plots
Statistical comparison tables

Note: Output files are not included in this repository because they are generated dynamically from local experimental datasets.

# Example results 

O-Maze Open-Arm Occupancy
Open Field Center Occupancy
Cross-Assay Behavioral Correlation

Figures shown are representative outputs generated from the analysis workflow.
