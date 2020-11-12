# QCB455Project
Final project for QCB 455. We have replicated parts of the analysis from the research paper found at https://elifesciences.org/articles/19760.

**Link to the Figure 3 replication R Markdown [here](http://notes.anthonyhein.com/Fig3_Replication.html)**

Horlbeck MA, Gilbert LA, Villalta JE, Adamson B, Pak RA, Chen Y, Fields AP, Park CY, Corn JE, Kampmann M, Weissman JS. __Compact and highly active next-generation libraries for CRISPR-mediated gene repression and activation__. Elife. 2016 Sep 23;5:e19760. doi: 10.7554/eLife.19760. PMID: 27661255; PMCID: PMC5094855.

`Featurization.ipynb` shows featurization steps for sgRNA data. This pipeline is described in Fig 1a. of the paper linked above. Features include: Distance to TSS (primary and secondary, downstream and upstream), sgRNA length, template/sense strand, longest consecutive run of each base, overall nucleotide composition (% of A, C, T, G, GC, CA, AG), nucleotides and dimers at each position.

Other features which were not directly available to us where linked by the paper to the following sources:
1. RNA folding metric package: https://scicrunch.org/resolver/SCR_008550
2. Custom Python scripts with the module bxpython (v0.5.0, https://github.com/bxlab/bx-python) to extract the processed continuous signal from the following BigWig files obtained from the ENCODE consortium: MNase-seq https://www.encodeproject.org/files/ENCFF000VNN/ (Michael Snyder lab, Stanford University), DNase-seq https://www.encodeproject.org/files/ENCFF000SVY/ (Gregory Crawford lab, Duke University), and FAIRE-seq https://www.encodeproject.org/files/ENCFF000TLU/ (Jason Lieb lab, University of North Carolina) (ENCODE Project Consortium, 2012). 

Authors: Anthony Hein, Manya Kapoor, Briana Macedo
