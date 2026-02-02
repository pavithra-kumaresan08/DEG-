# DEG-
This repository contains R scripts for RNA-seq differential gene expression analysis using DESeq2, applied to identify genes associated with chlorantraniliprole resistance in Plutella xylostella.
This repository contains R scripts for RNA-seq differential gene expression (DEG) analysis using DESeq2, followed by integration with WGCNA co-expression modules to identify chlorantraniliprole resistance–associated genes in Plutella xylostella. The workflow includes DEG identification, visualization, module–DEG overlap analysis, and network export for Cytoscape.

🔬 Workflow Steps
Step 1: Load Required Libraries

The analysis uses R packages for RNA-seq analysis, data manipulation, visualization, and network analysis.

DESeq2

tidyverse

ggplot2

ggrepel

reshape2

VennDiagram

grid

Step 2: Input Data Preparation

Raw RNA-seq count matrix (counts.csv)

Sample metadata defining experimental groups:

SC: Susceptible Control

ST: Susceptible Treated

RC: Resistant Control

RT: Resistant Treated

Samples are assigned to groups and used to construct the DESeq2 design matrix.

Step 3: Differential Gene Expression Analysis

LStep 4: DEG Output Files

Step 5: DEG Visualization

MA plot for expression changes

Volcano plots:

All DEGs

Significant DEGs (Up/Down regulated)

Top significant genes labeled using ggrepel

Step 6: Integration with WGCNA Modules

Step 7: Module–DEG Overlap Outputs

Step 8: Network Preparation for Cytoscape

Step 9: Venn Diagram Analysis

Venn diagrams are generated to visualize overlap between:

WGCNA module genes

Significant DEGs

This helps highlight resistance-associated hub genes.
