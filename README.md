# project1-sequence-analysis
This is a simulation of the next generation sequencing data analysis work flow. Sequencing reads are compared with a known reference sequence to identify nucleotide differences, or mismatches. These mismatches can then be used to identify and characterise mutations within the sequenced DNA.


Title and Purpose: this program analyses the next generation sequencing data by comparing DNA reads with a reference sequence. The aim of this program is to investigate whether sampels that are exposed to a genotoxic treatment have more DNA mismatches than untreated samples. 

How to run the program: Firstly, open the jupyter notebook in Google Colab, then upload the reference.txt and reads.csv files and finally run the cells in order from top to bottom to complete the analysis and filling the code when prompted. 

Inputs and outputs: the program uses two input files, reference.txt which contains the reference DNA sequence and reads.csv which contains 6,000 DNA reads from six samples. three of the smpales are treated and three are untreated (control). The program displays summary tables, substitution couns and the three position of the most matches. The program identifies the valid and invalid reads and calculate mismatch percentages. 

Code Design: i divided the program into seperate functions to make it easier to understand and test. For example, validate_read() checks whether a sequence has the correct length and contains only valid DNA bases and find_mutations() identifies differences between the sequence and reference. I also chose to store the results in a dictionary because it helps me organise informaiton using descriptive keys such as valid_reads. Thi smakeds the results easier to access than storing everything in a list without labels. Another decsion was not include invalid reads from mismatch calculations while still recording their errors. this prevents incorrect sequences from affecting the results. 

Testing: fisrt i tested find_mutations() using short DNA sequences with a known difference to chekc that the correct postion and bases were identified. Secondly i tested summarise_samples() with an empty input to chekcthat it returned an empty dictionary without errors. Lastly, I tested compare_positions() using the sample data with known percentages to check that it calculated the correct group means, differences and statistical results. 
