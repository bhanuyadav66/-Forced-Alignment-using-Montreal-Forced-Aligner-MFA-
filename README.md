# Forced Alignment using Montreal Forced Aligner (MFA)

## Objective
The objective of this assignment is to perform forced alignment between speech audio and text transcripts using Montreal Forced Aligner (MFA) and analyze word and phoneme boundaries.

## Tools and Software Used
- Montreal Forced Aligner (MFA) v3.3.9
- Anaconda (Python environment)
- Praat software (for visualization)
- English US ARPA acoustic model and dictionary

## Dataset Preparation
1. A dataset containing audio (.wav) files and transcript (.txt) files was provided.
2. All audio and transcript files were placed in a single folder named **dataset**.
3. Each transcript file had the same name as its corresponding audio file.
4. Transcripts were converted to uppercase.
5. All punctuation marks were removed to avoid alignment errors.

Example:
F2BJRL1.wav  
F2BJRL1.txt  

## Installation and Setup
1. Installed Anaconda.
2. Created MFA environment:
