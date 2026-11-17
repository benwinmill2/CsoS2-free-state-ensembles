# Project 3 notes

## Setup log
- GOAL: Which positions in the CsoS2 [IV]TG motifs and in the CsoS1A binding pocket are under selection, and which substitutions would break or tolerate binding? The output is a ranked, hypothesis-grade map of variants plus a proposed test panel. That is the same kind of sequence-to-function output the Pinney lab’s work is built around, and it feeds your DeGrado-oriented design project later.

Anchors from Ni et al. (2023): the motif contacts the CsoS1A β-strand through His79 and main-chain hydrogen bonds, repeats about every 8 residues, and is highly conserved across the CsoS2 family. Replacing all [IV]TG motifs with AAA gave only T = 4 and T = 3 shells. That experimental negative is your validation target. 
- PDB 8B12 is the T=9 shell structure from Ni et al. 2023 (Nature Communications, 14:5512, DOI 10.1038/s41467-023-41211-y)
- This paper was repeatedly referenced as sanity checks for the simulation 
- 712-869 is the C terminal region of CsoS2 which (in addition to the middle region, Oltrogge et al. (2020) ) binds the CsoS1A hexamers 
- Chain IDs:
         A-F: form one complete CsoS1A hexamer
         G-I: form half of a neighboring CsoS1A hexamer at the hexamer-hexamer interface ( chain G is slightly shorter because C terminal tail wasnt resolved)
         X: CsoS2 protein 
- chains functions by pulling all the real (non water non ligand) residues from the file
- seq joins the 1 character representation of each residue into a full string
- print prints the chain ID, its length, range, and the number of [IV]TG motifs it contains
- motif contacts takes a chain id (ex. "X"), a distance in angstroms, and a 3 residue motif, and returns the amount of atoms within your length from it according to the cryo EM file. 
- if rb.get_parent().id != s2_chain: throws away any atoms part of your motif 
- 


