Checklist for Data Analysis Scripts
-----------------------------------

Documentation and Organization
==============================

	- [ ] Is there a readme? 
	- [ ] Are the scripts and data dependencies organized sensibly in a folder? 
	- [ ] Is the code written in small, manageable chunks? 
	- [ ] Are the dependencies (data, packages, other scripts) clearly documented? 
	- [ ] Is the intent of the analysis clear from the documentation? 

Code Structure
==============

	- [ ] Is the code properly indented, using a reasonable line length, and is an editor with syntax highlighting used?
	- [ ] Does the code follow a consistent style and formatting?
	- [ ] Does the code follow the DRY principle and use functions? 
	- [ ] Are functions and variable names informative? Can you guess what a function does by its name and arguments?
	- [ ] Are there redundant or unused variables? 
	- [ ] Are there repeated blocks of code that can be made into a function?
	- [ ] Can the code easily handle changes/updates to the inputs (e.g. data updates)? 
	
Data Reading and Cleaning
=========================

	- [ ] Is there any data manipulation done outside of the script, eg in Excel? 
	- [ ] Are missing values identified and handled correctly? 
	- [ ] Are merge operations done correctly using an appropriate key? Any chances for scrambling of data? 
	- [ ] Are transformations to variables done correctly? 

Analysis Methods
================

	- [ ] Are methods reinvented that are implemented in an existing (high quality) package?
	- [ ] Are the algorithm settings/defaults known and correct? 
	- [ ] Does the analysis do what is intended? 
	- [ ] Are there any issues with convergence or other numerical problems? 
	- [ ] Do the results rely on random number generation? If so, is set.seed() used? 
	- [ ] Are there any slow running blocks that need to be optimized? (The need may depend on how frequently the script will be run)
	- [ ] Does the analysis successfully address the needs of the project? 
	
Output
=======

	- [ ] Do the results rely on any external tools for output? 
	- [ ] Do downstream modifications need to be made to the output? 
	- [ ] What is the intended product of the analysis (report, paper, presentation, etc.) and how does the script address it? 
