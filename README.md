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
   conda create -n aligner montreal-forced-aligner python=3.11
   conda activate aligner
3. Verified installation:
    mfa version 3.3.9
4. Downloaded pretrained dictionary and acoustic model:
    mfa model download dictionary english_us_arpa
    mfa model download acoustic english_us_arpa
## Running Forced Alignment
1. Navigated to project folder and executed:
   mfa align dataset english_us_arpa english_us_arpa output
   
This command generated TextGrid files with word and phoneme timestamps.

## Output
After successful execution:
- TextGrid files generated for each audio file
- alignment_analysis file generated
- Output stored in **output** folder

The TextGrid files contain:
- Word-level alignment
- Phoneme-level alignment
- Start and end timestamps

## Visualization
Praat software was used to visualize alignment:
1. Opened audio and TextGrid in Praat.
2. Observed waveform, word boundaries, and phoneme boundaries.
3. Verified correct alignment between speech and transcript.

## OOV (Out-of-Vocabulary) Handling
OOV words are words not present in the pronunciation dictionary.

These can be handled by:
- Adding new words manually to dictionary
- Using MFA G2P model to generate pronunciation
- Using pretrained dictionaries

Alignment was successfully completed using the default english_us_arpa dictionary.

## Conclusion
The forced alignment process was successfully performed using Montreal Forced Aligner. TextGrid files were generated and visualized using Praat. This experiment demonstrated how speech audio can be aligned with transcripts at word and phoneme level.

   
