# Genomic-study-for-color-blindness

This project analyzes genome sequence data to determine color blindness configurations by aligning reads to reference sequences and analyzing red/green gene exon mappings.

## Problem Overview

Given:
- 3 million genome reads (subset of 150M total reads)
- X chromosome reference sequence (150M bases)
- BWT last column and reference pointers for X chromosome
- Red and green gene exon locations in X chromosome

The goal is to:
1. Align reads to reference sequence allowing up to 2 mismatches
2. Count reads mapping to red/green gene exons:
   - 1 count for unambiguous mappings
   - 0.5 count for ambiguous mappings
3. Calculate probabilities for different red-green configurations
4. Determine most likely color blindness configuration

## Implementation Details

The solution uses:
- BWT-based sequence alignment
- Checkpointing for efficient BWT lookups
- Probabilistic analysis of gene configurations

Key processing steps:
1. Read preprocessing ('N' -> 'A' conversion)
2. BWT-based read alignment with mismatch handling
3. Exon mapping and read counting
4. Configuration probability calculations

## Results

The analysis:
- Processes millions of sequence reads
- Maps reads to gene exons
- Calculates configuration probabilities
- Identifies most likely color blindness configuration

## Usage

Run the Jupyter notebook to:
1. Load and preprocess input data
2. Perform sequence alignments
3. Analyze gene mappings
4. Generate probability results

## Requirements

- Python 3.x
- Jupyter Notebook
- Required libraries (numpy, pandas)

## Data Files

- X chromosome sequence data (~715MB)
- BWT index files
- Gene location reference files
