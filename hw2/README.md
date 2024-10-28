## **HW2**
### **Article reconstruction: "Comparative Genomics and Chromosome Evolution in Lepidoptera”**

> Phylogenetics, lepidoptera evolution.

Studies of phylogenetic trees play an important role in understanding the evolutionary history and genetic structure of organisms In this work, the main objective was to construct a phylogenetic tree for 210 butterfly species based on the sequence of a single gene, COI, and then compare the resulting tree with the phylogenetic tree described in a recent study. The original tree from the paper was constructed using more than 5000 orthologs and allowed the study of large evolutionary processes such as chromosome rearrangements, fusions and fissions.

The COI gene (cytochrome c-oxidase subunit I) was chosen because it is a standard barcode marker for species identification in phylogenetic studies and is widely used in molecular systematics. COI sequences are available for many species, making this gene convenient for interspecific comparisons. 

**Limitations of the approach**

When using only a single gene, especially a mitochondrial gene, there is a risk of obtaining a simplified and potentially incomplete picture of evolutionary relationships, as such trees may not account for chromosomal rearrangements and complex adaptations reflected in nuclear genes. 

**Hypothesis **

It was hypothesized that even a single COI gene could provide, at least in a simplified form, insight into the evolutionary structure of groups comparable to the results of multi-gene analysis. 

---
**Steps to achive our goal "Article reproduction":**

1. Download all fasta for gene COI ("Downloading_data" notebook)
2. Sequnces alignment (MAFFT)
3. Check the alignments (Ugene)
4. Using Trimal for trimming the alignments if necessary (and it's necessary)
5. Check outgroup IDs
6. Use IQTree to get the tree (outgroup!)
7. Rename the tree ("Downloading_data" notebook)
8. Visualize the tree
9. Tanglegram to campare trees (phylotree)

---
**Results **

The COI-constructed tree differed from the one provided in the paper, which became particularly apparent when compared using a taglogram. Visualization showed discrepancies in a number of clusters and branches, which can be explained as insufficient data to account for all evolutionary processes. 

*Figure 1. Lepidoptera phylogeny tree reconstruction*
<img width="882" alt="Снимок экрана 2024-10-29 в 00 03 31" src="https://github.com/user-attachments/assets/ffd14935-af57-4c5f-a72a-be4afdbafa86">

*Figure 2. Co-phylogenetic tanglegram. Left side is tree that was made in research paper, right side - my reconstruction*
<img width="666" alt="Снимок экрана 2024-10-29 в 00 04 53" src="https://github.com/user-attachments/assets/bbac2e80-bb9f-4a0c-855b-0c7ed26c5032">

---

**Conclusions **

This analysis confirmed that a phylogenetic tree based on a single gene can only provide a partial view of evolutionary processes. This emphasizes the importance of using a multi-gene approach to more accurately construct phylogenetic relationships (at least the use of partitioning). The choice of COI was justified but showed its limitations. 
