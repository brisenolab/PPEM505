# Bioinformatics Manual for Sequence Analysis
## Fundamental of Plant Pathology PPEM505 – Module 2 
### Ricardo I. Alcalá Briseño Ph. D.

<img width="1200" height="103" alt="image" src="https://github.com/brisenolab/PPEM505/blob/main/images/alignment.png" />


### How to construct a phylogenetic analysis 101
Materials for the _in silico_ lab: Class of fundamentals of plant pathogens PPEM505.

## 1) Get homologous sequences
After you get your sequence(s), the first option would be to download homologous sequences from a database, like NCBI (although, it might be possible you can use specialized databases, e.g. [UNITE](https://unite.ut.ee/), [silva RNA](https://www.arb-silva.de/) or [organism databases](https://busco.ezlab.org/)). 

After your fetch the sequences and select the most relevant for your organism of study, you can download a `.fasta` file.

## 2) Align homologous sequences

There are multiple ways to align your sequences, you can use graphic user interface (GUI), or the commmand line interface (CLI).

> First, download the software [MEGA](https://www.megasoftware.net/) \
> _Check you have installed the MEGA software._

### Making Alignments in MEGA (GUI)

Manual for sequence analysis using MEGA 12.

**Step 1.** Click on data and open a file, select the document (will start with ITS.fasta), then select align.
**Step 2.** Evaluate visually the alignment \
• Confirm sequence type (DNA vs protein) \
• Check orientation (reverse complements, partial sequences) \
• Inspect sequence length variation \
• Identify low-quality or ambiguous regions (N’s, gaps, truncations) \
- Are these sequences expected to be homologous across their full length?

**Step 3.** Select the alignment method and run \
• Global vs local expectations \
• Pairwise vs multiple sequence alignment \
• Default scoring vs adjusted gap penalties \
• Nucleotide vs amino-acid alignment \
MEGA have three heuristics models: ClustalW / MUSCLE \
Default parameters encode assumptions

**Step 4.** Visual evaluation of the alignment \
• Over-gapping at sequence ends consider removing \
• Internal gap clusters it's okay \
• Conserved motifs are usually well aligned \
• Considered regions driven by single sequences

> Note: Your alignment needs to have equal lenghts, and have the less amount of variation, althoug, it depends of the sequence.

**Step 5.** Identify and handle ambiguous regions \
• Mask or trim poorly aligned blocks \
• Decide whether gaps are informative or noise \
• Avoid automated trimming without justification, you night to justify your decisitions.

**Step 6.** Save alignment with metadata \
• Save your alignment method \
• Note gap penalties or other modifications \
• Software version \
• Date 
> Example: ssRNA_Puccinia_MEGA12-clustal-aln_v1-260218.fata

## 3) Run your model test to find the best maximum likelihood evolutionary model \
• Click on models and run find the best model \
• Select the model with the least lowest negative log likelihood score \
• Usully, is the model with the minimum AICc or BIC score \
• Record the selected model to use in your maximum likelihood phylogenetic tree

## 4) Construct a maximum likelihood phylogenetic tree \
• Select trees and a window will open, then \
• Test with bootstrap, and at least 1000 bootstrap replicates \
• Choose the substitution model you obtain from model test \
  • Remember, +I stands for invariant sites (I) \
              +G stands for gamma distribution (G)  \
              +I+G, you are selecting both rates and patterns \
• It will take some time, and phylogenetic analysis are somewhat computational intensive, so make sure your computer is plug to current. \
• Save your tree - as png or SVG if you want to edited using Adobe Illustrator or [Affinity Designer](https://www.affinity.studio/) a free option for vector graphics).

## Write your report:
• Make your report ready for publication. \
• Cite your software, sequences, databases, etc. \
• Make sure your figure is manuscript ready and do not forget the figure caption.



> Download the data for today's analysis (4 fasta files: ITS, rRNA, root for rRNA, RdRP, and more) or `git clone` this repository.

```git
git clone https://github.com/brisenolab/PPEM505/
```

If you haven't installed `git`, type `sudo apt install git` in Windows or `brew install git` in Mac. If you haven't installed [brew](https://brew.sh/), install it first.
