**RepSeq_TCRanalysis**
>Project in [Bioinformatics Institute](https://bioinf.me/) with the TCR Analysis of Rep-Seq data


# Studying population frequencies of T-cell receptor (TCR) alleles using immune repertoire sequencing

***Students:** Bagrova Olga & Vinogradova Sofiya*

***Supervisors:** Vlasova Elizaveta & Shugay Mikhail*

# Table of contents

   * [Introduction](#introduction)
   * [Project Structure](#project-structure)
   * [How to install](#how-to-install)
   * [Results](#results)
      * [Deletion gene-candidates](#deletion-gene-candidates)
      * [Haplotypes identification](#haplotypes-identification)
      * [Co-expression patterns](#co-expression-patterns)
      * [Thymic selection](#thymic-selection)
   * [Conclusions](#conclusions)
   * [Future plans](#future-plans)
   * [Contacts](#contacts)
   * [References](#references)


## Introduction

T cells are the essential part of human adaptive immune system, with their specificity derived from the unique T cell receptors (TCR). TCR generation involves a process called V(D)J recombination. Through this mechanism, specific V, D, and J genes are chosen from the TCR alpha (TRA) and TCR beta (TRB) loci and are then rearranged to form the TCRα and TCRβ chains of the receptor, respectively [^1].

**Aim:**
Analyze TCR repertoire distributions for large cohort of donors to find deletions, common and rare haplotypes and other effects.

**Objectives:**

* Detect TRA/TRB deletions and amplifications 
* Analyze coherence of amplifications and deletions forming haplotypes in TRA and TRB genes
* Analyze co-expression patterns in V-V and J-J pairs for TRA/TRB genes
* Analyze co-expression patterns between TRA and TRB genes
* Compare found patterns between populations


## Project Structure
- `./data` *directory with raw and corrected data for cohort I [^2] and cohort II [^3]*
- `./notebooks` *code for an analysis of data*
- `./pictures` *pictures with the results* 
- `README.md`


## How to install
```
git clone git@github.com:Olga-Bagrova/RepSeq_TCRanalysis.git
cd RepSeq_TCRanalysis
```


## Results

### Deletion gene-candidates

![TRBV gene usage on population scale histograms](/pictures/TRBV_hist_gene_usage.png)

The majority of genes showed expected unimodal distributions (*TRBV7-7*), some revealed bimodal (*TRBV11-3*) or trimodal (*TRBV6-3*) patterns. An investigation whether the distribution modality could be explained by donor’s race showed statistically significant differences in gene usage between Asian and Caucasian populations for *TRBV7-4* gene, as well as between Latino and Caucasian populations for *TRBV4-3* gene.

### Haplotypes identification

![TRAJ gene usage on population scale clustermaps](/pictures/TRAJ_clustermap_maxnorm.png)

An interesting pattern has been discovered for the *TRAJ21* gene (the fifth column on the left). It has zero usage in most donors but high usage in a few individuals. This may also reflect a possible deletion of this gene in the population.

### Co-expression patterns

![TRBJ correlations within TRα/β](/pictures/TRBJ_corr.png)

One of the unexpected results was the high Pearson correlation of the TRBJ genes: genes within the TRBJ1 and TRBJ2 groups are highly correlated. Also, some TRBJ2 (*TRBJ2-6*, *TRBJ2-7*) genes had high correlation coefficients with the TRBJ1 group.
A similar effect was not found in the second cohort. The analysis of the association of the corresponding genes with MHC variants did not yield significant results.

Additionally, the correlations of gene usage between the TRA and TRB chains did not show significant correlations.

### Thymic selection

![TRBV nonfunctional vs only functional sequences](/pictures/TRBV_scatter_of_nf.png)

Some genes showed a higher usage of nf sequences compared to of ones. While some of these genes were recognized as pseudogenes, others had no known non-functionality. It was suggested that negative thymic selection against such CDR3 might be [^4]. The same patterns were observed for the cohort-II. The Kolmogorov-Smirnov test was used to compare distributions.


## Conclusions

This study systematically analysed TCR repertoires in large cohorts from Russian and American populations.

* **Gene usage histograms** revealed significant variations in V and J gene usage across TCRα and TCRβ chains, potentially influenced by ethnicity. 
* **Hierarchical clustering** uncovered rare haplotypes (TRAJ21), indicating unique immune repertoire characteristics within subgroups of donors. 
* **Investigation into functional versus non-functional** CDR3 sequences suggested certain V genes associated with higher frequency non-functional sequences may undergo negative thymic selection, implying a possible biological mechanism where certain gene configurations are selectively disadvantageous. 

*Such T cell repertoire analysis is crucial for practical applications, as understanding the nuances of adaptive immunity can directly influence the selection of targets for receptor-based therapies.*


## Future plans

* To test the available hypotheses explaining the found patterns.
* Integrate additional data to discover new hypotheses and confirm existing ones.


## Contacts:

* **Bagrova Olga**: Olga-Bagrova [:octocat:](https://github.com/Olga-Bagrova)
* **Vinogradova Sofiya**: sofiyaga57 [:octocat:](https://github.com/sofiyaga57)
* **Vlasova Elizaveta**: VEK239 [:octocat:](https://github.com/VEK239)
* **Shugay Mikhail**: mikessh [:octocat:](https://github.com/mikessh) mikhail.shugay@gmail.com


### References

[^1]:	Murphy, K., & Weaver, C. (2016). Janeway’s Immunobiology. W.W. Norton & Company. doi 10.1201/9781315533247
[^2]:	Vlasova, E. K., Nekrasova, A. I., Komkov, A. Y., Izraelson, M., Snigir, E. A., Mitrofanov, S. I., Yudin, V. S., Makarov, V. v., Keskinov, A. A., Korneeva, D., Pivnyuk, A., Shelyakin, P. v., Mamedov, I. Z., Rebrikov, D. v., Chudakov, D. M., Yudin, S. M., Skvortsova, V. I., Britanova, O. v., & Shugay, M. A. (2023). Robust detection of SARS-CoV-2 exposure in the population using T-cell repertoire profiling. BioRxiv, doi 10.1101/2023.11.08.566227
[^3]:	Emerson, R. O., DeWitt, W. S., Vignali, M., Gravley, J., Hu, J. K., Osborne, E. J., Desmarais, C., Klinger, M., Carlson, C. S., Hansen, J. A., Rieder, M., & Robins, H. S. (2017). Immunosequencing identifies signatures of cytomegalovirus exposure history and HLA-mediated effects on the T cell repertoire. Nature Genetics, 49(5), 659–665. doi 10.1038/ng.3822
[^4]:	Manfras, B. J., Terjung, D., Boehm, B. O. (1999). Non-productive human TCR beta chain genes represent V-D-J diversity before selection upon function: insight into biased usage of TCRBD and TCRBJ genes and diversity of CDR3 region length. Hum Immunol, 60(11), 1090-100. doi: 10.1016/s0198-8859(99)00099-3.
