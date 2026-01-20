# Topology-Constrained Metric Matching (TCMM) Data Repository

## Branch Length Estimation:
### 1) S100 Dataset (Tabatabaee et al. 2023):
The original dataset is available at [https://github.com/ytabatabaee/CASTLES-paper](https://github.com/ytabatabaee/CASTLES-paper). We provide the results of our experiments in the `TCMM-ASTRAL-SU-Results` directory.

Here is the description of each file in this directory:
- `TCMM-ASTRAL-SU-Results/*/truegenetrees`: True gene trees for each replicate.
- `TCMM-ASTRAL-SU-Results/*/fasttree_genetrees_[length]_non`: Estimated gene trees from `length`bp-long sequences.
- `TCMM-ASTRAL-SU-Results/*/castlespro_truegenetrees_s_tree.trees`: True species tree with SU branch lengths assigned by CASTLES-Pro.
- `TCMM-ASTRAL-SU-Results/*/castlespro_fasttree_genetrees_[length]_non_s_tree.trees`: Estimated species tree from `TCMM-ASTRAL-SU-Results/*/fasttree_genetrees_[length]_non` with SU branch lengths assigned by CASTLES-Pro.
- `TCMM-ASTRAL-SU-Results/*/TCMM_castlespro_truegenetrees_s_tree_lam_[lambda].trees`: True species tree with SU branch lengths assigned by TCMM (lambda = `[lambda]`). The input species tree and gene trees to TCMM are `TCMM-ASTRAL-SU-Results/*/castlespro_truegenetrees_s_tree.trees` and `TCMM-ASTRAL-SU-Results/*/truegenetrees`, respectively.
- `TCMM-ASTRAL-SU-Results/*/TCMM_castlespro_truegenetrees_s_tree_lam_best.trees`: True species tree with SU branch lengths assigned by TCMM (automatic lambda selection). The input species tree and gene trees to TCMM are `TCMM-ASTRAL-SU-Results/*/castlespro_truegenetrees_s_tree.trees` and `TCMM-ASTRAL-SU-Results/*/truegenetrees`, respectively.
- `TCMM-ASTRAL-SU-Results/*/TCMM_castlespro_fasttree_genetrees_[length]_non_s_tree_lam_[lambda].trees`: Estimated species tree with SU branch lengths assigned by TCMM (lambda = `[lambda]`). The input species tree and gene trees to TCMM are `TCMM-ASTRAL-SU-Results/*/castlespro_fasttree_genetrees_[length]_non_s_tree.trees` and `TCMM-ASTRAL-SU-Results/*/fasttree_genetrees_[length]_non`, respectively.
- `TCMM-ASTRAL-SU-Results/*/TCMM_castlespro_fasttree_genetrees_[length]_non_s_tree_lam_best.trees`: Estimated species tree with SU branch lengths assigned by TCMM (automatic lambda selection). The input species tree and gene trees to TCMM are `TCMM-ASTRAL-SU-Results/*/castlespro_fasttree_genetrees_[length]_non_s_tree.trees` and `TCMM-ASTRAL-SU-Results/*/fasttree_genetrees_[length]_non`, respectively.

### 2) HGT Dataset:
The results of the simulated dataset is provided in the `TCMM-HGT-SU-Results`.

Here is the description of each file in this directory:
- `TCMM-HGT-SU-Results/[model]/*/estimatedgenetre`: Estimated gene trees.
- `TCMM-HGT-SU-Results/[model]/*/castlespro_estimatedgenetre_s_tree.trees`: Species tree with SU branch lengths assigned by CASTLES-Pro.
- `TCMM-HGT-SU-Results/[model]/*/TCMM_castlespro_estimatedgenetre_lam_[lambda].trees`: Species tree with SU branch lengths assigned by TCMM (lambda = `[lambda]`). The input species tree and gene trees to TCMM are `TCMM-HGT-SU-Results/[model]/*/castlespro_estimatedgenetre_s_tree.trees` and `TCMM-HGT-SU-Results/[model]/*/estimatedgenetre`, respectively.
- `TCMM-HGT-SU-Results/[model]/*/TCMM_castlespro_estimatedgenetre_lam_best.trees`: Species tree with SU branch lengths assigned by TCMM (lambda = automatic lambda selection). The input species tree and gene trees to TCMM are `TCMM-HGT-SU-Results/[model]/*/castlespro_estimatedgenetre_s_tree.trees` and `TCMM-HGT-SU-Results/[model]/*/estimatedgenetre`, respectively.

### 3) Bacterial Dataset (Moody et al. 2022):
The results of the prokaryotic dataset is provided in the `bacterial_dataset` directory. The original dataset can be found at [https://doi.org/10.6084/m9.figshare.13395470](https://doi.org/10.6084/m9.figshare.13395470).

Here is the description of each file in this directory:
- `bacterial_dataset/core_genes.tre`: Estimated core gene trees.
- `bacterial_dataset/non_ribosomal_genes.tre`: Estimated non-robisomal gene trees.
- `bacterial_dataset/castles_pro_core_genes.tre`: Estimated species tree from core gene trees with SU branch lengths assigned by CASTLES-Pro.
- `bacterial_dataset/castles_pro_non_ribosomal.tre`: Estimated species tree from non-ribosomal gene trees with SU branch lengths assigned by CASTLES-Pro.
- `bacterial_dataset/per_gene_castles_pro_core_genes_lam_[lambda].trees`: Estimated species tree from core gene trees with SU branch lengths assigned by TCMM (lambda = `[lambda]`). The input species tree and gene trees to TCMM are `bacterial_dataset/castles_pro_core_genes.tre` and `bacterial_dataset/core_genes.tre`, respectively.
- `bacterial_dataset/per_gene_castles_pro_non_ribosomal_genes_lam_[lambda].trees`: Estimated species tree from non-ribosomal gene trees with SU branch lengths assigned by TCMM (lambda = `[lambda]`). The input species tree and gene trees to TCMM are `bacterial_dataset/castles_pro_non_ribosomal.tre` and `bacterial_dataset/non_ribosomal_genes.tre`, respectively.

### 4) WoL Dataset (Zhu et al. 2019):
The results of the WoL dataset is provided in the `WoL` directory. The original dataest can be found at [https://github.com/biocore/wol/tree/master/data](https://github.com/biocore/wol/tree/master/data).

Here is the description of each file in this directory:
- `WoL/castles_pro_wol.tre`: Estimated species tree with SU branch lengths assigned by CASTLES-Pro.
- `WoL/genetrees/p[geneID].nwk`: Estimated individual gene trees.
- `WoL/TCMM-results/p[geneID]_lam_[lambda].trees`: Estimated species tree with SU branch lengths assigned by TCMM (lambda = `[lambda]`). The input species tree and gene trees to TCMM are `WoL/castles_pro_wol.tre` and `WoL/genetrees/p[geneID].nwk`, respectively.

## Outlier Detection:

### 1) S200-perturbed Dataset:
The outlier detection results for this dataset are provided in `S200-perturbed` directory. Here is a description of each file in this directory:
- `S200-perturbed/true_outliers.txt`: The ground truth outliers for this dataset. Columns are replicate, gene tree, and species, respectively.
- `S200-perturbed/outliers_gene_vs_gene_k1.5.csv`: The outliers outputted by PhylteR and TCMM+PhylteR for k=1.5 (the value used in the paper).
- `S200-perturbed/TreeShrink_outliers.txt`: The outliers reported by TreeShrink.
- `S200-perturbed/*/s_tree.tree`: True species tree in the unit of number of generations.
- `S200-perturbed/*/truegenetrees_100`: True gene trees (the first 100 from the original dataset).
- `S200-perturbed/*/modifiedTrees_100`: Modified gene trees after introducing outliers.
- `S200-perturbed/*/modifiedTrees_100_lam_[lambda].trees`: TCMM output on modeified gene trees (lambda = [lambda]). Note that [lambda] = true means original gene trees before running TCMM.

### 2) S100 Dataset (Tabatabaee et al. 2023):
The outlier detection results for the S100 dataset are provided in the `TCMM-ASTRAL-Outlier-Results` directory. Here is a description of each file in this directory:
- `TCMM-ASTRAL-Outlier-Results/*/truegenetrees_100`: The first 100 true gene trees.
- `TCMM-ASTRAL-Outlier-Results/*/fasttree_genetrees_[length]_non_100`: The first 100 estimated gene trees from `length`bp-long sequences.
- `TCMM-ASTRAL-Outlier-Results/*/truegenetrees_100_lam_[lambda].trees`: Modified true gene trees by TCMM (lambda = [lambda]). The input gene trees to TCMM are `TCMM-ASTRAL-SU-Results/*/outlier_detection/truegenetrees_100`.
- `TCMM-ASTRAL-Outlier-Results/*/fasttree_genetrees_[length]_non_100_lam_[lambda].trees`: Modified estimated gene trees by TCMM (lambda = [lambda]). The input gene trees to TCMM are `TCMM-ASTRAL-SU-Results/*/outlier_detection/fasttree_genetrees_[length]_non_100`.
- `TCMM-ASTRAL-Outlier-Results/*/TCMM_outliers_truegenetrees.csv`: Detected outliers for the modified true gene trees by TCMM.
- `TCMM-ASTRAL-Outlier-Results/*/TCMM_outliers_fasttreegenetrees.csv`: Detected outliers for the modified estimated gene trees by TCMM.
- `TCMM-ASTRAL-Outlier-Results/*/TreeShrink_outliers_truegenetrees.csv`: Detected outliers for the modified true gene trees by TreeShrink.
- `TCMM-ASTRAL-Outlier-Results/*/TreeShrink_outliers_fasttreegenetrees.csv`: Detected outliers for the modified estimated gene trees by TreeShrink.

### 3) TreeShrink Dataset (Mai and Mirarab 2018):
The original dataest can be found at [https://github.com/uym2/TreeShrink](https://github.com/uym2/TreeShrink). The results of TCMM outlier detection can be found in the `TreeShrink_data` directory. This directory contains six biological datasets: `TreeShrink_data/Plants`, `TreeShrink_data/Mammals`, `TreeShrink_data/Frogs`, `TreeShrink_data/Insects`, `TreeShrink_data/XenRouse`, and `TreeShrink_data/XenCannon`. Here is a description of each file in these directories:
- `TreeShrink_data/[data]/unfiltered.trees`: Estimated gene trees.
- `TreeShrink_data/[data]/gene_vs_gene_unfiltered_lam_[lambda].trees`: Modified estimated gene trees by TCMM (lambda = [lambda]). The input gene trees to TCMM are `TreeShrink_data/[data]/unfiltered.trees`.
- `TreeShrink_data/[data]/TCMM_outliers.csv`: Detected outliers for the modified estimated gene trees by TCMM.
- `TreeShrink_data/[data]/TreeShrink_outliers.txt`: Detected outliers for the modified estimated gene trees by TreeShrink.
