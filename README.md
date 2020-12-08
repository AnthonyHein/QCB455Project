# QCB455Project
Final project for QCB 455. We have replicated parts of the analysis from the research paper found at https://elifesciences.org/articles/19760.

Horlbeck MA, Gilbert LA, Villalta JE, Adamson B, Pak RA, Chen Y, Fields AP, Park CY, Corn
JE, Kampmann M, Weissman JS. Compact and highly active next-generation libraries for CRISPRmediated gene repression and activation. Elife. 2016 Sep 23;5:e19760

# **Link to the Figure 3 replication R Markdown [here](http://notes.anthonyhein.com/Fig3_Replication.html)**
Also available in `Fig3_Replication.Rmd`, which does not show figures. This work was done by Manya Kapoor.

# Featurization 
`Featurization.ipynb` shows featurization steps for sgRNA data. This pipeline is described in Fig 1a. of the paper linked above. Features include: Distance to TSS (primary and secondary, downstream and upstream), sgRNA length, template/sense strand, longest consecutive run of each base, overall nucleotide composition (% of A, C, T, G, GC, CA, AG), nucleotides and dimers at each position. Features not available to us included DNAse-seq / MNase-seq / FAIRE-seq signal, sgRNA overall folding free energy, RNA pairing at each position. All multiclass or numerical features were binned with `Binning.ipynb`. Anthony Hein and Briana Macedo contributed equally to `Featurization.ipynb` while Briana Macedo was the sole author of `Binning.ipynb`.


# Fitting and Machine Learning
`Fitting.ipynb` provides code for the Elastic Net Linear Regression training a 5-fold cross validation training, as well as the plotting code for Figure 1. Anthony Hein was the primary author for this file, though it leverages feautrization achieved jointly by Anthony Hein and Briana Macedo.

# Prediction Weights
`Prediction_weights.ipynb`contains code for extracting features within a category, and the code for plotting the contribution of these features given the coefficients in our machine learning model. This was achieved by Briana Macedo with marginal debugging help from Anthony Hein.


## Data Files

Small data files are found in this public repository. Larger `.csv` files are stored in Google Drive and accessible via [this](https://drive.google.com/drive/folders/1hBk8SSjvc3XTXX40mjz9nQmcTlPxaT0S?usp=sharing) link.

### Authors: Anthony Hein, Manya Kapoor, Briana Macedo

