# manuscript-Il6-biologics-serum

## Panorama files

- Panorama project dashboard can be found here: https://panoramaweb.org/MacCoss/Catherine%20Sniezek/T1D%20Serum%20Treatment/project-begin.view
  - Includes initial data analysis and writeup of project
  - Skyline file used for analysis is found here under the name "T1D_Serum_EV_Treatment_DIANNv1.9.2-imputed_2025-01-19_12-35-35.sky.zip"
  - Raw files can be found under RawFiles/QuantFiles

## Description of files

- IL6 serum biologics.Rmd: R markdown file containing scripts for data manipulation and visualization
- IL6 serum biologics.prism: prism file containing figures and analyses not made in R (figures 1E-F, 2B, 2D)
#### Input

- 250121_T1D_Serum_EV_Treatment.csv: Peptide abundances exported from Skyline document grid
- 250125_meta.csv: table containing metadata for each sample analyzed. Paired samples collected from the same patient are indicated by Patient number. Acronyms are defines as:
	  - "SB" - Siltuximab pre-treatment
	  - "ST" - Siltuximab post-treatment
	  - "TB" - Tocilizumab pre-treatment
	  - "TT" - Tociilizumab post-treatment
- 250124_treatment_peptides.csv: Manually curated list of quantitative peptides from Siltuximab and Tocilizumab therapeutic antibodies
- Jensen_COMPARTMENTS.gmt: gene set containing Jensen's compartments 
- ReactomePathways.gmt: gene set containing Reactome pathways
- siltux_log2FC.rnk: fgsea-compatible list of proteins, ordered by limma-derived log2FC of siltuximab effect
- siltux_R.rnk: fgsea-compatible list of proteins, ordered by Pearson R correlation to siltuximab quantitation
- siltux_rho_rnk: fgsea-compatible list of proteins, ordered by spearman rho correlation to siltuximab quantitation
- tocil_log2FC.rnk: fgsea-compatible list of proteins, ordered by limma-derived log2FC of tocilizumab effect
- tocil_R.rnk: fgsea-compatible list of proteins, ordered by Pearson R correlation to tocilizumab quantitation
- tocil_rho.rnk: fgsea-compatible list of proteins, ordered by spearman rho correlation to tocilizumab quantitation
- Uniprot_to_gene_name.csv: dataframe to match uniprot accession numbers to proper gene names

#### Output
- 251125_normed_proteins.csv: dataframe containing equalize-median normalized proteins, including proper gene name
- **fgsea_log2FC_reactome.xlsx:** file containing fgsea results; **Figure 3C**
- fgsea_R_compartment.csv: dataframe containing fgsea results; figure S2
- limma_results.csv: dataframe containing results from limma analysis **Figure 2A-B**

