# cross-systems-behavioral-analytics
End-to-end R workflow analyzing cross-system behavioral data with repeated-measures and independent cohort designs to assess treatment effects and metric robustness.

# Problem statement
This project investigates whether pharmacological blockade of two receptor subtypes in the brain produces distinct behavioral effects in mice across multiple anxiety-related measurement systems, and whether these effects generalize consistently across independent assays or remain context-specific.

# Data Description
The dataset consists of behavioral measurements from two mouse genotypes (β4E61C and β2E61C) assigned to either control or pharmacological treatment groups. Animals were evaluated across three assays (Elevated O-Maze, Open Field, and Light–Dark Box) generating time-based, transition-based, and locomotor metrics. The O-Maze and Open Field were conducted on the same animals, enabling within-subject cross-assay analysis, whereas the Light–Dark Box used an independent cohort. Sample sizes ranged from 10–12 animals per group, with unequal group sizes handled using appropriate parametric or non-parametric statistical tests. The resulting dataset combines repeated-measures and between-subject structures, allowing both group-level comparisons and cross-system validation analyses.

# Key techniques used
Data cleaning ?
Feature engineering of behavioral metrics (e.g., time allocation, transition counts, locomotor indicators)
Group comparison tests (Welch t-tests, Wilcoxon rank-sum tests)
Repeated-measures analysis for within-subject assay comparisons
Correlation analysis across behavioral systems for matched subjects
Data visualization using time allocation and behavioral distribution plots
Handling of unbalanced sample sizes and non-normal distributions

# How to run the code: 

#


