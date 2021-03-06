
Motivation
----------

As statisticians, we generate lots of software, in the form of data cleaning scripts, analysis scripts, R packages, and implementations of new methods. However, most of us have not received any formal training in software development and most of what we learned about R was "on the job". Furthermore, despite the fact that the results of our analyses and resulting papers rely on it, much of this software is never seen by the broader scientific community. There is also no formal process for code checking, as there is in programming, even though the results of our code get published. 

Our domain-specific knowledge puts us in the unique position to review and understand each others' code. We can learn from each other to improve the quality and foster collaboration on the software aspects of our research. 

What I plan to do
------------------

Assemble small groups (3-4 reviewers) to sit down and review a member's code for a specific project. The goal of the review will be pre-specified and targeted. For example: 

- Ensure the accuracy and reproducibility of an data analysis script
- Verify that a new method is implemented correctly
- Optimize a piece of code that is running slowly 
	
The review itself will be structured and somewhat formal. This is to ensure that the reviews are useful and efficient. There are some guidelines out there for general code review, but developing the structure and guidelines for statistical code review will be an iterative process. 

What I need help with
---------------------

- Developing the initial guidelines and checklists for the review process. I've got a start going [here](http://github.com/sachsmc/stats-code-review). 
- Developing education materials and discussions on best-practices and useful tools (e.g., git, Rstudio, devtools).
- Volunteers with code that they would like others to review. 
- Volunteers to serve on small review groups. 

Links to checklists
-----------------------------

- [Data Analysis Checklist](http://github.com/sachsmc/stats-code-review/blob/master/Checklists/analysis-checklist.md)
- [R Optimization Checklist](http://github.com/sachsmc/stats-code-review/blob/master/Checklists/r-optimize-checklist.md)

Other Resources

- [Code Review Guide by Mozilla Science](https://mozillascience.github.io/codeReview/intro.html)
- [Code Review for and by Scientists, Petre and Wilson](http://arxiv.org/pdf/1407.5648v2.pdf)
- [Smartbear 11 best practices for code review](http://smartbear.com/smartbear/media/pdfs/wp-cc-11-best-practices-of-peer-code-review.pdf)
- [Troubling Trends in Scientific Software Use, Joppa et al.](http://www.sciencemag.org/content/340/6134/814.full)
