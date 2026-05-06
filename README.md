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

## Repository Contents

- `crosss_analysis_code.Rmd` — main behavioral analytics workflow in R Markdown
- `figures/` — representative output figures generated from the analysis


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
Openfield Distance Traveled 
Cross-Assay Behavioral Correlation

Note: Figures are derived from analysis outputs generated in R and were post-processed in Adobe Illustrator for publication-quality formatting.

# Key Results

## O-Maze Anxiety-Related Behavior

![O-Maze Results](figures/omaze_open_arm_results.png)

**Figure 1.** Time spent in the open arms of the O-maze for β4E61C (CTRL: n = 10; MPEG4Ch-treated: n = 12) and β2E61C (CTRL: n = 10; MPEG4Ch-treated: n = 12) mice. Statistical comparisons were performed using Welch two-sample t-tests. A significant reduction in open-arm occupancy was observed in MPEG4Ch-treated β4E61C mice (t = –2.40, *p = 0.029), whereas no significant effect was detected in β2E61C mice (t = 0.77, p = 0.455).

These results suggest that MPEG4Ch treatment selectively increased anxiety-like behavior in β4E61C mice, reflected by reduced exploration of exposed areas in the O-maze.

---

## Open Field Behavioral Measures

![Open Field Results](figures/openfield_results.png)

**Figure 2.** Open field behavioral parameters measured for β4E61C and β2E61C mice under CTRL and MPEG4Ch treatment conditions. Parameters included total distance traveled, transitions from the periphery to the center, and time spent in the center zone.

For β4E61C mice, no significant treatment effects were observed for distance traveled (t = –1.49, p = 0.159), center transitions (t = –1.16, p = 0.258), or time spent in the center (t = –0.76, p = 0.457). In β2E61C mice, no differences were found for locomotion (t = –0.15, p = 0.882), while MPEG4Ch-treated animals showed reduced time spent in the center (Wilcoxon rank-sum test: W = 18, *p = 0.015), consistent with increased anxiety-like behavior.

These findings indicate genotype-dependent behavioral effects, with anxiety-related phenotypes emerging primarily in β2E61C mice during the Open Field assay.

---

## Cross-Assay Behavioral Correlation

![Cross-Assay Correlation](figures/cross_assay_correlation.png)

**Figure 3.** Correlation between anxiety-related measures in the O-maze and Open Field assays. Scatterplots show the relationship between time spent in the open arms of the O-maze and time spent in the center of the Open Field for individual mice across experimental groups: β4E61C CTRL (n = 10), β4E61C MPEG4Ch-treated (n = 12), β2E61C CTRL (n = 12), and β2E61C MPEG4Ch-treated (n = 12).

A significant positive Spearman correlation was detected only in MPEG4Ch-treated β4E61C mice (ρ = 0.643, *p = 0.028), suggesting consistency of anxiety-related behavioral responses across assays within this treatment-genotype condition.

---

Overall, the analysis demonstrates assay- and genotype-dependent behavioral effects following MPEG4Ch treatment, with convergent anxiety-related phenotypes observed across independent behavioral systems.
