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

Low-count genes are filtered.

Differential expression analysis is performed using DESeq2.

Contrast performed: RT vs ST

Significant DEGs identified using:

Adjusted p-value (FDR) < 0.05

|log2 Fold Change| > 1

Step 4: DEG Output Files

The following files are generated:

DEG_RT_vs_ST_all.csv – all genes with DESeq2 statistics

DEG_RT_vs_ST_significant.csv – significant DEGs only

DEG_RT_vs_ST_significant_with_direction.csv – DEGs classified as up- or down-regulated

Step 5: DEG Visualization

MA plot for expression changes

Volcano plots:

All DEGs

Significant DEGs (Up/Down regulated)

Top significant genes labeled using ggrepel

Step 6: Integration with WGCNA Modules

High-confidence resistance-associated genes from WGCNA modules are integrated with DEG results.

Modules analyzed:

Blue module

Turquoise module

For each module:

Overlap between significant DEGs and module genes is identified

Overlapping genes are classified as up- or down-regulated

Step 7: Module–DEG Overlap Outputs

For each module, the following files are generated:

Overlapping gene lists

Full DEG statistics for overlapping genes

Separate counts of up- and down-regulated genes

Example outputs:

blue_module_DEG_overlap_genes.csv

blue_module_DEG_overlap_full_info.csv

turquoise_module_DEG_overlap_genes.csv

turquoise_module_DEG_overlap_full_info.csv

Step 8: Network Preparation for Cytoscape

Topological Overlap Matrix (TOM) is filtered

Low-weight edges removed

Network edge and node files exported for visualization in Cytoscape

Example outputs:

*_module_DEG_overlap_edges.csv

*_module_DEG_overlap_nodes.csv

Step 9: Venn Diagram Analysis

Venn diagrams are generated to visualize overlap between:

WGCNA module genes

Significant DEGs

This helps highlight resistance-associated hub genes.
