# Replicate_of_comparison_of_single_cell_RNA_seq_methods
 This repository reproduces key figures and analyses from the study “Comparison of single-cell RNA-sequencing methods for human immune profiling.”
The goal is to replicate the preprocessing, quality control, and visualization workflows described in the paper using Scanpy, Seaborn, and Matplotlib in Python. There was no need to import the package that authors created (besca) to reproduce these figures, which saved time and space while running the analysis.

Below are the figures reproduced:
<img width="1439" height="425" alt="image" src="https://github.com/user-attachments/assets/8d0610f6-c3bf-4a8b-a34e-459b450bcaac" />
<img width="1439" height="425" alt="image" src="https://github.com/user-attachments/assets/e196e9c2-4a64-40d8-bd87-43e9945d76a1" />
<img width="1439" height="425" alt="image" src="https://github.com/user-attachments/assets/4cb9e57d-9d0f-4b69-8580-e548011a9e43" />
# Figure 3A
<img width="931" height="826" alt="image" src="https://github.com/user-attachments/assets/d91fdffd-632f-4372-a90d-743a73e77b72" />
<img width="913" height="820" alt="image" src="https://github.com/user-attachments/assets/000879e0-7b58-42b4-b24b-3ef5ab4d9240" />
<img width="1015" height="821" alt="image" src="https://github.com/user-attachments/assets/3be2ea23-73e5-4ec7-9d78-35cfd3f53a40" />


Note: clusters were done with scanpy package rather than besca package (created by authors), similar results are shown.


The project evaluates how different scRNA-seq technologies perform when profiling human immune cells, focusing on:
- Library quality and cell-level QC metrics (figure 2A-C)
- Expression stability across technologies and cell types (Figure 2D)
- Cross-technology clustering consistency across cell types and tissues (Figure 3A)

Below are the details to create an environment to run the code:

$ conda create -n scRNA_replicate python=3.11
$ conda activate scRNA_replicate
$ pip install scanpy seaborn matplotlib pandas numpy scipy
$ jupyter notebook <file name: Analysis_figure2.ipynb or Analysis_figure_3A.ipynb>


# Input files required
From the following link (https://zenodo.org/records/15373124)
- annotated.all_merged.h5ad
- raw.all_merged.h5ad

  # Summary of results
  From these key figures we can see that they evaluated data quality by examining three metrics: total UMI counts, the number of genes detected per cell, and the proportion of mitochondrial gene expression (Fig 2). These metrics help identify low-quality or stressed cells, as well as cells that may have experienced membrane leakage during processing. The results showed that Evercode platform had the lowest mitochondrial fractions, followed by Flex. The clustering showed that cells grouped primarily according to their cell type and the sequencing platform used (Fig 3A). Whithin these broader clusters, additional separation emerged based on the sample preparation method, specifically, whether the cells originated from PBMC or RBC-depleted samples (figure not shown, but can be reproduced by running the code). Overall, this paper shows that monitoring neutrophil gene expression provides valuable insights into disease biology, supports diagnostic development, and informs clinical trial design. It shows that neutrophils are particularly sensitive to handling procedures, including processing, storage, and transport, making high-quality single-cell analysis challenging, but not impossible. The paper showed three techniques (10X Genomics, Parse Biosciences, HIVE) for profiling human blood-derived neutrophils. The comparitive evalution showed that all three platforms successfully generated high-quality data and effectively captured neutrophil transcriptomes. As a result, the authors outline a robust scRNA-seq workflow suitable for clinical trials. 



