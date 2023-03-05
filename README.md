# MHC-prediction
Welcome!
Here are the supplementary files and notes for  ***A systematic assessment of MHC Ⅱ peptide presentation prediction methods.***

**Supplementary Data S1** summarizes the utilities of existing 18 methods for MHC-peptide-binding prediction, divided into three categories: scoring functions, consensus methods and machine learning approaches. 

**Supplementary Data S2** lists the positive and negative datasets used for benchmarking. 

**Supplementary Data S3** shows the details of the prediction outputs of each method.

**Supplementary Data S4** is the AUC calculated for each method.

**Supplementary Data S5** shows the amino acid positional preferences for allotype-specific peptide ligands.

**Supplementary Data S6** To facilitate users to select methods for better prediction, we search the best BACC score for 11 predictors. We calculated the maximum BACC score for each method for the whole dataset and each subset with different lengths and HLA proteins to select the best cutoff for binary prediction. The F1 scores are also listed here.

**Supplementary S7** For the eleven servers, we have tested the prediction using peptides binding with 20 HLA- II allotypes in independent databases. Due the training datasets and algorithms used, not all methods work for all peptides ranging from 11 to 19 aa long binding with all 20 HLA- II allotypes.

Methods are able to predict in All 20 HLA-Ⅱ allotypes: NetMHCpan-3.2，NetMHCpan-4.0，NetMHCpan-4.1，MHCnuggets；The prediction range of other servers are as follows: 

1.	**SMM-align(12~18mers)**: HLA-DPA101:03-DPB102:01,HLA-DPA102:01-DPB101:01,HLA-DQA103:01-DQB103:02,HLA-DRB103:01,HLA-DRB104:01,HLA-DRB115:01,HLA-DRB501:01.
2.	**BERTMHC(11~19mers)**: HLA-DPA101:03-DPB102:01,HLA-DPA101:03-DPB103:01,HLA-DPA101:03-DPB104:01,HLA-DPA101:03-DPB104:01,HLA-DPA101:03-DPB104:02,HLA-DPA102:01-DPB101:01,HLA-DPA102:01-DPB109:01,HLA-DPA102:01-DPB110:01,HLA-DPA102:01-DPB113:01,HLA-DPA102:01-DPB114:01,HLA-DPA102:02-DPB105:01,HLA-DQA103:01-DQB103:02.
3.	**IEDB consensus(12~18mers)**：HLA-DPA101:03-DPB102:01,HLA-DPA102:01-DPB101:01，HLA-DQA103:01-DQB103:02，HLA-DRB103:01,HLA-DRB104:01,HLA-DRB115:01,HLA-DRB501:01，HLA-DRB101:02，HLA-DRB107:01，HLA-DRB108:01.
4.	**MARIA(11~19mers)**: HLA-DQA1_03_01_DQB1_03_02,HLA-DRB101:02,HLA-DRB103:01,HLA-DRB104:01,HLA-DRB107:01，HLA-DRB108:01, HLA-DRB115:01, HLA-DRB302:02, HLA-DRB401:01, HLA-DRB501:01.
5.	**MHCII3D(11~19mers)**: HLA-DRB103:01,HLA-DRB104:01,HLA-DRB115:01,HLA-DRB501:01，HLA-DRB101:02，HLA-DRB107:01，HLA-DRB108:01.
6.	**NetMHCII-2.3(11~19mers)**: HLA-DPA101:03-DPB102:01,HLA-DPA101:03-DPB103:01,HLA-DPA101:03-DPB104:01,HLA-DPA101:03-DPB104:01,HLA-DPA101:03-DPB104:02,HLA-DPA102:01-DPB110:01,HLA-DPA102:01-DPB114:01,HLA-DQA103:01-DQB103:02,HLA-DRB103:01,HLA-DRB104:01,HLA-DRB115:01,HLA-DRB501:01，HLA-DRB107:01，HLA-DRB108:01.
7.	**MixMHC2pred (11~19mers)**: Except for 11mer's HLA Ⅱ allotypes, all other peptides in our database can be predicted.

Then, we use webservers /softwares to make predictions. Different methods have distinct outputs. Scores used to calculate the AUC curves could be seen as follows: BERTMHC: affinity_pred, MARIA: MARIA raw scores, MHCnuggets: IC50, MixMHC2pred: %Rank_best, NetMHCIIpan-4.1 and NetMHCIIpan-4.0: %Rank_EL, NetMHCII-2.3, NetMHCII-3.2: 1-log50k(aff), NetMHCII, IEDB consensus: percentile_rank, MHCII3D: rank.
