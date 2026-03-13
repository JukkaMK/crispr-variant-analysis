# CRISPR Variant Analysis

This repository demonstrates a lightweight and interpretable workflow for exploring and prioritizing genetic variants in a CRISPR-related context using Python and Jupyter notebooks.

The focus is on biological interpretation of variant effects rather than building a complex analysis pipeline.

## Background

Understanding the functional impact of genetic variants is essential in genome editing and gene therapy research.

## Data

A small demonstration dataset of annotated variants is included:

data/variants_demo.tsv

The dataset contains information such as:

- gene
- variant consequence
- predicted impact
- allele frequency

## Analysis workflow

The analysis is implemented in two notebooks:

1. **01_basic_variant_exploration.ipynb**  
   Exploration of variant annotations and dataset structure.

2. **02_variant_scoring_demo.ipynb**  
   Demonstrates a simple scoring approach combining:
   - predicted variant impact
   - allele frequency
   - CRISPR target gene prioritization

## Results

The variant scoring workflow prioritizes variants based on predicted functional impact and allele frequency.

Variants with **HIGH predicted impact** receive the highest base scores, particularly when combined with **low allele frequency**, reflecting the increased likelihood that rare variants have stronger biological effects.

The CRISPR candidate prioritization step further highlights variants occurring in genes commonly studied in genome editing contexts. In this demonstration dataset, variants in genes such as **BRCA1** and **PCSK9** appear among the highest-ranked candidates.

Overall, the scoring approach illustrates how simple biological heuristics can be combined to prioritize potentially relevant variants for downstream genome editing or functional studies.

## Key findings

- High-impact variants dominate the top scoring candidates.
- Rare variants receive higher prioritization.
- Combining variant-level scoring with gene-level prioritization highlights biologically relevant targets.

## Visualizations

The notebooks generate several plots:

- variant score distribution
- CRISPR candidate counts
- gene × impact heatmap

## Project structure

```
crispr-variant-analysis/
│
├─ data/
│   └─ variants_demo.tsv
│
├─ notebooks/
│   ├─ 01_basic_variant_exploration.ipynb
│   └─ 02_variant_scoring_demo.ipynb
│
├─ src/
├─ .gitignore
└─ README.md
```

## Requirements

Python packages used:

- pandas
- numpy
- matplotlib
- jupyterasets
