# Genomic-study-for-color-blindness

This project analyzes genome sequence data to determine color blindness configurations by aligning reads to reference sequences and analyzing red/green gene exon mappings.

## Problem Overview

Given:
- 3 million genome reads (subset of 150M total reads) # Input data description
- X chromosome reference sequence (150M bases) # Reference sequence details
- BWT last column and reference pointers for X chromosome # BWT data for alignment
- Red and green gene exon locations in X chromosome # Gene location data

The goal is to:
1. Align reads to reference sequence allowing up to 2 mismatches # Main alignment task
2. Count reads mapping to red/green gene exons: # Read counting rules
   - 1 count for unambiguous mappings
   - 0.5 count for ambiguous mappings
3. Calculate probabilities for different red-green configurations # Probability analysis
4. Determine most likely color blindness configuration # Final determination

## Implementation Details

The solution uses:
- BWT-based sequence alignment # Core alignment algorithm
- Checkpointing for efficient BWT lookups # Performance optimization
- Probabilistic analysis of gene configurations # Statistical analysis

Key processing steps:
1. Read preprocessing ('N' -> 'A' conversion) # Data preparation
2. BWT-based read alignment with mismatch handling # Alignment process  
3. Exon mapping and read counting # Read analysis
4. Configuration probability calculations # Statistical calculations

## Results

The analysis:
- Processes millions of sequence reads # Scale of analysis
- Maps reads to gene exons # Mapping results
- Calculates configuration probabilities # Probability outputs
- Identifies most likely color blindness configuration # Final conclusion

## Usage

Run the Jupyter notebook to:
1. Load and preprocess input data # Data loading
2. Perform sequence alignments # Core processing
3. Analyze gene mappings # Analysis step
4. Generate probability results # Results generation

## Requirements

- Python 3.x # Language requirement
- Jupyter Notebook # Development environment
- Required libraries (numpy, pandas) # Dependencies

## Data Files

- X chromosome sequence data (~715MB) # Input data
- BWT index files # Alignment data
- Gene location reference files # Gene data
