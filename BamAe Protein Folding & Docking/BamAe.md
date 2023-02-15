# BamA-epitope Transmembrane Folding & Docking

## [Predicted structure of the BamA-epitope sequence expressed in the producer cell](BamAe Protein Folding & Docking/BamAe Docking.png)

Explanation for why we chose to express BamA-epitope instead of the full BamA transmembrane protein and how we modelled the structure:

Structure predicted using ColabFold, annotated with the outer, transmembrane, and periplasmic labels predicted using DeepTMHMM. The signal sequence does not denote the MalE translocon peptide – it is the region connecting loops 6 and 7 to the other regions of the full BamA protein. Structure was plotted using the Protein Imager tool (Tomasello, Armenia & Molla, 2020).B. The DeepTMHMM prediction results per residue – assigned probabilities in the hidden Markov model and most likely topology/label.

We employed several structural analysis and protein folding methods to determine if we could express the BamA epitope region by itself in a stable manner, in absence of the other BamA domains. Thus, we first determined the folding motif of BamA loops 6 and 7 (periplasmic domain 5) using ColabFold (Mirdita et al., 2022) to ensure we get the same conformation (periplasm bit, β-barrel transmembrane region, outside region with variable loops) in absence of the other loops in the BamA structure to ensure our epitope folds correctly.

Using a deep learning prediction tool based on a pre-trained protein transformer model – DeepTMHMM (Hallgren et al., 2022), we predicted the topology across a membrane for our structure (periplasm, β-barrel, outer) and plotted them on the final structure (Figure A2.1. A). Lastly, following a review of the available literature, we concluded that β-barrel membrane proteins can be inserted in the outer membrane using the same BamA-BAM complex, therefore our structure with a single β-barrel region should be incorporated in the OM as well, as long as we first incorporate a Sec translocon for periplasmic translocation (Doyle & Bernstein, 2019; Zhang & Han, 2016). Therefore, we will only be expressing the loop 6-7 (periplasmic region 5) structure in our system, denoted as BamA-epitope 

## [Docked BamA-epitope – CdiA and binding interface](BamAe Docking.png)

Docked CdiA – BamA-epitope complex structure. 

The binding interface represents residues less than 5 Å apart for the two protein. BamA-epitope was predicted using ColabFold; CdiA was accessed using the PDB ID 6CP8. Structure was plotted using the Protein Imager tool (Tomasello, Armenia & Molla, 2020)

We also wanted to ensure that the CdiA structure expressed in the EC3006 E.coli strain (killer strain) binds the outer membrane region of the BamA-epitope structure obtained above. Using the Z-DOCK docking server (Pierce et al., 2014, we have determined the interface residues (paratope-epitope) of the two interacting proteins, demonstrating that CdiA binds the exposed surface (on the outer membrane) of the single β-barrel BamA-epitope protein.
