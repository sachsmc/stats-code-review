Checklist for Optimization of R Code
====================================

Cost analysis
-------------
Not all code needs to be optimized. Think about how many times the code will be run and how long it will take to recode in a faster way. If it takes 2 hours to recode a complicated algorithm, then it may not be worth it for a simple one-off analysis. It might be worth it if you are running 10,000 simulations. 

[Relevant XKCD](https://xkcd.com/1205/)

- How many times will this code be run?
- How much effort have you put into optimization already? 
- Are there risks of breaking functional code by trying to be clever?
- Do you have tests in place to ensure that the code is working properly?

Profiling
-----------

Use profiling to identify bottlenecks. 

```r
Rprof("profile.out")
## slow code
Rprof(NULL)
summaryRprof("profile.out")
```

Loops and Vectorization
-----------------------

- [ ] Can `colSums` or `rowSums` be used instead of `apply`/loops?
- [ ] Are vectors/lists preallocated prior to for loops? I.e., use `x[i] <- stuff` instead of `x <- append(x, stuff)`
- [ ] Are there any nested for loops? 
	- [ ] Can at least one of them be vectorized?
	- [ ] If not, consider using [Rcpp](http://dirk.eddelbuettel.com/code/rcpp.html)
- [ ] Is subsetting vectorized where possible?
- [ ] Can matrix algebra be used instead of looping?
	
Big data sets
--------------

- [ ] Using `read.csv` with `colClasses`?
- [ ] Are data frames copied or modified unnecessarily? 
- [ ] Can simpler data structures be used? E.g. vectors, matrices instead of lists/data frames
- [ ] If large data sets are being modified a lot, consider `data.table` or `dplyr`. 	

Other
-----------

- [ ] Can any `ifelse` be replaced by logical operators? 
- [ ] Can the number of function calls be reduced? Any recursive function calling going on?
- [ ] Can types be restricted and use low-level functions? E.g. use `.Internal(mean(x))` or `lm.fit`. 
- [ ] Can something be parallelized effectively?
- [ ] Try compiling fancy functions: `compile::cmpfun(function)` and `compile::compile(expression)`

