# Replicate_of_comparison_of_single_cell_RNA_seq_methods
 This repository reproduces key figures and analyses from the study “Comparison of single-cell RNA-sequencing methods for human immune profiling.”
The goal is to replicate the preprocessing, quality control, and visualization workflows described in the paper using Scanpy, Seaborn, and Matplotlib in Python.

The project evaluates how different scRNA-seq technologies perform when profiling human immune cells, focusing on:
- Library quality and cell-level QC metrics (figure 2A-C)
- Expression stability across technologies and cell types (Figure 2D)
- Cross-technology clustering consistency across cell types and tissues (Figure 3A)

Below are the details to create an environment to run the code:
$ conda create -n scRNA_replicate python=3.11
$ conda activate scRNA_replicate
$ pip install scanpy seaborn matplotlib pandas numpy scipy
