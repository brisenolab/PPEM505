# Bioinformatics Manual for Sequence Analysis
## Fundamental of Plant Pathology PPEM505 – Module 2 
### Ricardo I. Alcalá Briseño

<img width="1200" height="103" alt="image" src="https://github.com/brisenolab/PPEM505/blob/main/images/alignment.png" />

#### Manual for sequence analysis using MEGA 12.

First, download the software [MEGA](https://www.megasoftware.net/)

_Check you have installed the MEGA software._

Download the data for today's analysis (4 fasta files: ITS, rRNA, root for rRNA, RdRP) or `git clone` this repository.

```git
git clone https://github.com/brisenolab/PPEM505/
```

**Step 1.** Click on data and open a file, select the document (will start with ITS.fasta), then select align.
**Step 2.** Evaluate visually the alignment 
• Confirm sequence type (DNA vs protein)
• Check orientation (reverse complements, partial sequences)
• Inspect sequence length variation
• Identify low-quality or ambiguous regions (N’s, gaps, truncations)
- Are these sequences expected to be homologous across their full length?

**Step 3.** Select the alignment method and run
• Global vs local expectations
• Pairwise vs multiple sequence alignment
• Default scoring vs adjusted gap penalties
• Nucleotide vs amino-acid alignment
MEGA have three heuristics models: ClustalW / MUSCLE / MAFFT
Default parameters encode assumptions

**Step 4.** Visual evaluation of the alignment
• Over-gapping at sequence ends
• Internal gap clusters
• Misaligned conserved motifs
• Suspiciously perfect columns
• Regions driven by single sequences

**Step 5.** Identify and handle ambiguous regions
• Mask or trim poorly aligned blocks
• Decide whether gaps are informative or noise
• Avoid automated trimming without justification

**Step 6.** Save alignment with metadata
• Save your alignment method
• Note gap penalties or other modifications
• Software version
• Date
