# Intro
This pipeline integrates several bioinformatics tools/packages with the aim of facilitating the analysis of variant enrichment analysis (Deep mutational scanning data). Two approaches (command line and GUI) are provided. <br>
The statistical enrichment score is derived from Enrich2 results. 6 enrichment plots will be generated by default including 3 amino acids based and 3 codon based figures. Details regarding these plots can be found in Result session below.
This pipeline was tested on Mac OS X (10.13.6) with 16G memory.

This is version_2.0.
For trouble shooting, refer to script/troubleshooting.txt file.

# Usage
## Setup
First need to install the required packages and configure the environment by running the setup.sh. <br>
Download and unzip the git folder, open terminal, then: <br>
**cd scripts/** <br>
**bash setup.sh** <br>
It will take several minutes to install all components.

## GUI approach
After setup, do: <br>
**bash gui.sh** <br>
The GUI is self-explanatory, simply input wild type sequence, raw reads file and mutation sites, etc. accordingly and hit submit. It may take several minutes to run depending on your computational power.

## Command line approach
To learn how to use this mode, execute below for detailed instruction: <br>
**bash wrapper.sh -h** <br>
A configuration_template.txt file is provided inside script folder. <br>
Note that the configuration file setup is slightly different from that in version_1.0.

# Result
Results will be saved in plot_output folder. <br>
By default, 6 plots will be created: 3 are amino acid based and 3 are codon based. <br>
The first plot is raw figure containing all amino acid/codon columns and standard error, the second and third are simplified version of raw figure with empty columns removed and/or standard error bar removed. <br>
Sample output plots are provided in sample_plot_output folder. <br><br>
By default, all intermediate files will be kept, to free the space, save plot_output folder somewhere else for your own reference, then execute below to delete all intermediate files: <br>
**bash folder_clean.sh** <br>

# Update from version_1.0
1. Added in double mutation data mode. <br>
2. Added in multiple flag options: -m/-c/-s. Details see Usage. <br>
3. Optimized the visualization <br>
4. Fixed the path space bug.


**Question and bug report to Kai Hu: (kxh365@@@psu.edu).** <br>
