## Ugcg-KO Proteomics Analysis Files

*Proteomics_analysis-VBCS1122.Rmd*      
- Includes proteomics EDA + limma model + SGPV calculations 
- Requires proteomics data    
- Requires BioConductor libraries:
  - library(impute)      
  - library(pcaMethods)       
  - library(imputeLCMD)      
  - library(clusterProfiler)      
  - library(enrichplot)      
  - library(org.Mm.eg.db)      
- Creates "top_proteins.rds" file to be used in *global_gsea_results-VBCS1122.Rmd*     
- Creates "total_top.rds" file which includes "Gene.ID", "logFC", "P.Value","adj.P.Val", "SGPV" values      
- Includes volcano plots and p-values

*Global_gsea_results-VBCS1122.Rmd*      
- gseGO results + enrichment plots/tables        
- Requires "top_proteins.rds"      
- Creates *df_ME* of enriched pathways and associated genes       
- Creates *df_ME_melted* which is the long version of *df_ME*      
- Enrichment score dotplots + clusterprofiler treeplots which were not ultimately used      


*SGPV_CUSTOM_GSEA_VBCS-1122.Rmd*
- Includes tables + volcano plots for SGPVs     
- GSEA run on custom gene lists     
- Enrichment plots     
- List of most enriched genes in a pathway     


*Network_plots.Rmd* 
- Code for network plots using aPEAR package (doi: 10.1093/bioinformatics/btad672)            
- Averaged NES results         
- Max NES, cluster and pathways     
- List of enriched pathways and genes     