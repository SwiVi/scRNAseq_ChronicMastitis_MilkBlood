# Single-cell RNA sequencing characterization of Holstein cattle blood and milk immune cells during a chronic *Staphylococcus aureus* mastitis infection

Scripts found here are associated with single-cell RNA sequencing (scRNA-seq) analysis of the below work:

**Single-cell RNA sequencing characterization of Holstein cattle blood and milk immune cells during a chronic *Staphylococcus aureus* mastitis infection by Jayne E. Wiarda, Kaitlyn M. Sarlo Davila, Julian M. Trachsel, Crystal L. Loving, Paola Boggiotto, John D. Lippolis, and Ellie J. Putz**

Preprint link: *TBD*

Peer-reviewed publication: *TBD* **this work has not been accepted for peer-reviewed publication and is still subject to alterations**

## Repository organization
Scripts are sequentially ordered in number of execution and divided into modular sections. Some later scripts depend on data objects created in preceding scripts in order to execute. The below table gives a general overview of analysis performed in each step.
| File Name | Description |
| --- | --- |
| 01_tar.slurm | Untarring sequencing files |
| 02_cellranger_reference_prep_script.slurm | Creating reference genome for aligning and counting genes |
| 03_fastQC.slurm | Assessing sequencing read quality |
| 04_cellranger_map_individual.slurm | Mapping reads to reference genome to obtain gene count table |
| 05_check_mapping.R | Checking mapping outputs and metrics |
| 06_SoupX.R | Removing ambient RNA contamination |
| 07_scDblFinder.R | Identifying cell doublets |
| 08_CellGeneFiltering.R | Identifying and removing low-quality cells and non-expressed gene from the dataset |
| 09_NormalizationIntegrationDimReduction.R | Normalizing gene counts, integrating data, and performing dimensionality reductions |
| 10_ClusteringGeneQuery.R | Performing cell clustering and assessing gene expression profiles to annotate general cell types |
| 11_HierarchicalClustering.R | Performing heirarchical clustering to determine transcriptional relatedness of all cell clusters |
| 12_DGE.R | Identifying genes differentially expressed between all cell clusters, both overall and pairwise comparisons |
| 13_DA.R | Identifying cell neighborhoods with significantly different abundance between milk and blood samples |
| 14_BarPlots.R | Visualizing compositions within cell clusters, cell types, and overall samples |
| 15_GranulocyteSubsetting.R | Creating a data subset consisting of only granulocytes |
| 16_DGE_Granulocytes.R | Identifying differentially expressed genes between granulocyte clusters |
| 17_HierarchicalClustering_Granulocytes.R | Performing hierarchical clustering to determine transcriptional relatedness of only granulocyte clusters |
| 18_BarPiePlotting_Granulocytes.R | Visualizating compositions within only granulocytes at the level of cell clusters and phylogenetic nodes identified via hierarchical clustering |
| 19_MilkGranulocyteSignature.R | Creating a milk-enriched, granulocyte-specific gene signature through investigation of granulocyte differential gene expression results |
| 20_MilkGranulocyte_GeneSetEnrichment.R | Calculating and assessing gene set enrichment scores for granulocyte cells using the milk-enriched, granulocyte-specific gene signature |

## Additional materials
Additional data associated with this project can also be found as detailed below:
* Raw sequencing data can be found in the Sequence Read Archive (SRA) under BioProject ID PRJNA1114020 **(the sequencing data will be released upon publication)**
* Processed data objects can be found at ______ **(data will be available for download upon publication)**
* Data are available for online interactive query at ______ **(data will be available for download upon publication)**
