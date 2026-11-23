# ENCODE FCC Capstone Paper

This repository contains analysis code, processed results, and figure-generation notebooks supporting the ENCODE Functional Characterization Center (FCC) Capstone manuscript.

## Overview

The [ENCODE Project](https://www.encodeproject.org/) is a research consortium funded by the National Human Genome Research Institute (NHGRI) to identify and characterize functional elements in the human and mouse genomes.

As part of ENCODE Phase 4, the Functional Element Characterization Centers (FCCs) were established to develop and apply high-throughput approaches to characterize candidate regulatory elements.

The ENCODE FCC Capstone study brings together data from participating labs to systematically characterize cis-regulatory elements (CREs) in K562 cells. The study integrates four reporter assays (ATAC-STARR-seq, whole-genome STARR-seq, Lenti-MPRA, and Tiling MPRA) and two CRISPRi screening approaches (HCR-FlowFISH and growth screens).

We compare regulatory activity across assays to characterize assay concordance and assay-specific activity. We further integrate these results with genomic data, chromatin annotations, and chromatin interactions to investigate the properties of regulatory elements.

## Collaboration

This study is part of the ENCODE FCC collaborative effort, with participating labs contributing experimental datasets, computational analyses, and scientific interpretation.

More information about the ENCODE FCCs is available on the [NHGRI ENCODE Project website](https://www.genome.gov/Funded-Programs-Projects/ENCODE-Project-ENCyclopedia-Of-DNA-Elements).

## Functional Assay Overview

![Genome browser tracks at the LMO2 and HBE loci](./results/figures/fig.genome_track.fcc.chipseq.LMO2.HBE.png)

Tracks are displayed for the region containing LMO2, CAPRIN1 and CAT at the LMO2 locus, and for the HBE/HBG region of the β-globin locus, including the locus control region HS1-5. CRISPRi-HCR FlowFISH tracks represent gene-specific regulatory effects for the indicated target genes. Positive effects at a location indicate that CRISPRi disruption of the location decreases expression of the target gene. The CRISPRi-Growth track represents cell-fitness effects measured by CRISPRi perturbation. Positive effects at a location indicate that CRISPRi inhibition of the location decreases cell growth. STARR-seq and MPRA tracks represent regulatory activity measured by high-throughput reporter assays. Positive signals indicate that the region increases promoter-driven reporter expression. Reporter activity was measured across different assay designs, including ATAC-STARR-seq, whole-genome STARR-seq, tiling MPRA and LentiMPRA. STARR-seq tracks display pseudo-log2 fold changes, whereas tiling MPRA tracks display log2 fold changes. For LentiMPRA, z-scores displayed in the tracks were calculated relative to shuffled-sequence negative controls. K562 TSS annotations represent RefSeq transcription start sites, with one isoform selected per gene based on the highest K562 POLR2A signal. POLR2A signal and TSS annotations provide promoter-proximal transcriptional context. H3K27ac ChIP-seq signals provide enhancer context.

## Key Findings

![umap projection and cluster annotations of consensus regulatory elements](./results/figures/fig.region.umap.cluster.annotation.png)

Our study quantified the concordance and differences in regulatory activity across reporter assays and CRISPRi screens, identifying both shared and assay-specific patterns. Through sequence-based modeling, we identified transcription factor motifs associated with regulatory activity, including shared and assay-specific sequence features. By integrating functional measurements with genomic and chromatin features, we identified distinct clusters of regulatory elements associated with transcriptional activation, repression, and chromatin organization. We further examined enhancer-promoter interactions and found contact enrichment among regulatory elements with and without strong local CTCF/cohesin signatures. Together, these findings highlight the importance of sequence features, chromatin context, and three-dimensional genome organization in interpreting regulatory activity across functional assays.

## Interactive UMAP Explorer

We developed an interactive Shiny application to explore the chromatin features of 33,953 consensus CREs identified in our paper. The application visualizes UMAP projections of consensus CREs based on ENCODE K562 ChIP-seq profiles. Users can select individual transcription factors, chromatin regulators, and histone modifications from a dropdown menu to examine their signal distributions across the UMAP.

[Launch Interactive UMAP Explorer](https://kueiko.shinyapps.io/fcc_umap_cluster/)
