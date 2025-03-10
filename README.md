# Topology-Constrained Metric Matching (TCMM) Data Repository


## 1) S100 Dataset (Tabatabaee et al. 2023):
The original dataset is available at [Google Drive](https://drive.google.com/file/d/13ZrOhOliKCEpXebBlMg01WlRTGmnCXza/view). We provide the results of our experiments in the `TCMM-ASTRAL-SU-Results` directory.

Here is the description of each file in this directory:
- `TCMM-ASTRAL-SU-Results/*/truegenetrees`: True gene trees for each replicate.
- `TCMM-ASTRAL-SU-Results/*/fasttree_genetrees_[length]_non`: Estimated gene trees from `length`bp-long sequences.
- `TCMM-ASTRAL-SU-Results/*/castlespro_truegenetrees_s_tree.trees`: True species tree with SU branch lengths assigned by CASTLES-Pro.
- `TCMM-ASTRAL-SU-Results/*/castlespro_fasttree_genetrees_[length]_non_s_tree.trees`: Estimated species tree from `TCMM-ASTRAL-SU-Results/*/fasttree_genetrees_[length]_non` with SU branch lengths assigned by CASTLES-Pro.
- `TCMM-ASTRAL-SU-Results/*/TCMM_castlespro_truegenetrees_s_tree_lam_[lambda].trees`: True species tree with SU branch lengths assigned by TCMM (lambda = `[lambda]`). The input species tree and gene trees to TCMM are `TCMM-ASTRAL-SU-Results/*/castlespro_truegenetrees_s_tree.trees` and `TCMM-ASTRAL-SU-Results/*/truegenetrees`, respectively.
- `TCMM-ASTRAL-SU-Results/*/TCMM_castlespro_truegenetrees_s_tree_lam_best.trees`: True species tree with SU branch lengths assigned by TCMM (automatic lambda selection). The input species tree and gene trees to TCMM are `TCMM-ASTRAL-SU-Results/*/castlespro_truegenetrees_s_tree.trees` and `TCMM-ASTRAL-SU-Results/*/truegenetrees`, respectively.
- `TCMM-ASTRAL-SU-Results/*/TCMM_castlespro_fasttree_genetrees_[length]_non_s_tree_lam_[lambda].trees`: Estimated species tree with SU branch lengths assigned by TCMM (lambda = `[lambda]`). The input species tree and gene trees to TCMM are `TCMM-ASTRAL-SU-Results/*/castlespro_fasttree_genetrees_[length]_non_s_tree.trees` and `TCMM-ASTRAL-SU-Results/*/fasttree_genetrees_[length]_non`, respectively.
- `TCMM-ASTRAL-SU-Results/*/TCMM_castlespro_fasttree_genetrees_[length]_non_s_tree_lam_best.trees`: Estimated species tree with SU branch lengths assigned by TCMM (automatic lambda selection). The input species tree and gene trees to TCMM are `TCMM-ASTRAL-SU-Results/*/castlespro_fasttree_genetrees_[length]_non_s_tree.trees` and `TCMM-ASTRAL-SU-Results/*/fasttree_genetrees_[length]_non`, respectively.

## 2) HGT Dataset:
The results of the simulated dataset is provided in the `TCMM-HGT-SU-Results`.

Here is the description of each file in this directory:
- `TCMM-HGT-SU-Results/[model]/*/estimatedgenetre`: Estimated gene trees.
- `TCMM-HGT-SU-Results/[model]/*/castlespro_estimatedgenetre_s_tree.trees`: Species tree with SU branch lengths assigned by CASTLES-Pro.
- `TCMM-HGT-SU-Results/[model]/*/TCMM_castlespro_estimatedgenetre_lam_[lambda].trees`: Species tree with SU branch lengths assigned by TCMM (lambda = `[lambda]`). The input species tree and gene trees to TCMM are `TCMM-HGT-SU-Results/[model]/*/castlespro_estimatedgenetre_s_tree.trees` and `TCMM-HGT-SU-Results/[model]/*/estimatedgenetre`, respectively.
- `TCMM-HGT-SU-Results/[model]/*/TCMM_castlespro_estimatedgenetre_lam_best.trees`: Species tree with SU branch lengths assigned by TCMM (lambda = automatic lambda selection). The input species tree and gene trees to TCMM are `TCMM-HGT-SU-Results/[model]/*/castlespro_estimatedgenetre_s_tree.trees` and `TCMM-HGT-SU-Results/[model]/*/estimatedgenetre`, respectively.

## 3) Bacterial Dataset (Moody et al. 2022):
The results of the prokaryotic dataset is provided in the `bacterial_dataset` directory. The original dataset can be found at [https://doi.org/10.6084/m9.figshare.13395470](https://doi.org/10.6084/m9.figshare.13395470).

Here is the description of each file in this directory:
- `bacterial_dataset/core_genes.tre`: Estimated core gene trees.
- `bacterial_dataset/non_ribosomal_genes.tre`: Estimated non-robisomal gene trees.
- `bacterial_dataset/castles_pro_core_genes.tre`: Estimated species tree from core gene trees with SU branch lengths assigned by CASTLES-Pro.
- `bacterial_dataset/castles_pro_non_ribosomal.tre`: Estimated species tree from non-ribosomal gene trees with SU branch lengths assigned by CASTLES-Pro.
- `bacterial_dataset/per_gene_castles_pro_core_genes_lam_[lambda].trees`: Estimated species tree from core gene trees with SU branch lengths assigned by TCMM (lambda = `[lambda]`). The input species tree and gene trees to TCMM are `bacterial_dataset/castles_pro_core_genes.tre` and `bacterial_dataset/core_genes.tre`, respectively.
- `bacterial_dataset/per_gene_castles_pro_non_ribosomal_genes_lam_[lambda].trees`: Estimated species tree from non-ribosomal gene trees with SU branch lengths assigned by TCMM (lambda = `[lambda]`). The input species tree and gene trees to TCMM are `bacterial_dataset/castles_pro_non_ribosomal.tre` and `bacterial_dataset/non_ribosomal_genes.tre`, respectively.

## 4) WoL Dataset (Zhu et al. 2019):
The results of the WoL dataset is provided in the `WoL` directory. The original dataest can be found at [https://github.com/biocore/wol/tree/master/data](https://github.com/biocore/wol/tree/master/data).

Here is the description of each file in this directory:
- `WoL/castles_pro_wol.tre`: Estimated species tree with SU branch lengths assigned by CASTLES-Pro.
- `WoL/genetrees/p[geneID].nwk`: Estimated individual gene trees.
- `WoL/TCMM-results/p[geneID]_lam_[lambda].trees`: Estimated species tree with SU branch lengths assigned by TCMM (lambda = `[lambda]`). The input species tree and gene trees to TCMM are `WoL/castles_pro_wol.tre` and `WoL/genetrees/p[geneID].nwk`, respectively.
