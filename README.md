---
title: "AnalyticPmaxSource"
author: "MASKED"
date: "October 19, 2018"
knit: (function(inputFile, encoding) { rmarkdown::render(inputFile, encoding = encoding, output_file = paste0(dirname(inputFile),'/README.md')) })
output:
  html_document:
    keep_md: true
---

### Abstract

Research applying the behavioral economic demand framework is increasingly conducted across disciplines, as is research on improving the mathematical accuracy of demand metrics. At present, a variety of methods have been introduced to solve for the point of unit elasticity, or PMAX, in the Exponential model of demand; however, most of these methods vary in their potential for error due to being empirical approximations. Various methods for determining PMAX are presented here and a novel exact solution for PMAX in the Exponential model of demand is introduced. This solution provides an exact calculation of PMAX using the omega function, as algebraic solutions are not possible. This novel approach is introduced, discussed, and systematically compared to earlier methods for determining PMAX using computer simulations. Systematic comparison indicated that this new approach, an exact analytic solution for PMAX, provides results that are identical to computationally-intensive PMAX methods that directly evaluate the slope of the demand function. The exact analytic PMAX approach is reviewed, its calculations explained, and an easy-to-use web tool is provided to assist researchers in easily performing this calculation of PMAX. Implications for reducing potential sources of error are reviewed and future directions are also discussed.

[Markdown Source](https://github.com/miyamot0/AnalyticPmaxSource/blob/master/AnalyticPmaxSource.Rmd)

[Markdown Document](http://htmlpreview.github.com/?https://github.com/miyamot0/AnalyticPmaxSource/blob/master/AnalyticPmaxSource.html)

[Working Sample](http://www.smallnstats.com/index.php?page=PMAX)

### Credits

* Shawn Gilroy, Applied Behavioral Economics Laboratory, Louisiana State University [Github](https://github.com/miyamot0)

* Brent Kaplan, Carilion Research Institute, Virginia Polytechnic Institute and State University [Github](https://github.com/brentkaplan)

* Derek D. Reed, Applied Behavioral Economics Laboratory, University of Kansas (www.behavioraleconlab.com) [Github](https://github.com/derekdreed)

* Donald A. Hantula, Decision Making Laboratory, Temple University [Site](http://astro.temple.edu/~hantula/)

* Steven R. Hursh, Institutes for Behavior Resources, Johns Hopkins University School of Medicine

### Dependencies

- lambertW - Copyright Ben Bolker, port of Omega function from GSL (GPLv3).



### Table 1. Distribution of Unit Elasticity Estimates


|row             |      Q0|      Q1|      Q2|      Q3|       Q4|
|:---------------|-------:|-------:|-------:|-------:|--------:|
|AnalyticPmax    | 2.45655| 4.46924| 5.34454| 6.39693| 12.20367|
|HurshDerivative | 2.45655| 4.46924| 5.34454| 6.39693| 12.20367|
|HurshPmax       | 2.47089| 4.43210| 5.27383| 6.21326| 10.97175|
|ObservedPmax    | 1.50000| 5.00000| 6.00000| 8.00000| 20.00000|



|row             |      Q0|      Q1|      Q2|      Q3|       Q4|
|:---------------|-------:|-------:|-------:|-------:|--------:|
|AnalyticPmax    | 3.39425| 4.43719| 5.33661| 6.17661|  9.51373|
|HurshDerivative | 3.39425| 4.43719| 5.33661| 6.17661|  9.51373|
|HurshPmax       | 3.41699| 4.42331| 5.27033| 6.09176|  8.29142|
|ObservedPmax    | 2.50000| 5.00000| 6.50000| 8.00000| 20.00000|

### Table 2.


|                | HurshPmax| HurshDerivative| ObservedPmax| AnalyticPmax|
|:---------------|---------:|---------------:|------------:|------------:|
|HurshPmax       |   1.00000|         0.99584|      0.28346|      0.99584|
|HurshDerivative |   0.99584|         1.00000|      0.27524|      1.00000|
|ObservedPmax    |   0.28346|         0.27524|      1.00000|      0.27524|
|AnalyticPmax    |   0.99584|         1.00000|      0.27524|      1.00000|



|                | HurshPmax| HurshDerivative| ObservedPmax| AnalyticPmax|
|:---------------|---------:|---------------:|------------:|------------:|
|HurshPmax       |   1.00000|         0.99693|      0.43853|      0.99693|
|HurshDerivative |   0.99693|         1.00000|      0.43249|      1.00000|
|ObservedPmax    |   0.43853|         0.43249|      1.00000|      0.43249|
|AnalyticPmax    |   0.99693|         1.00000|      0.43249|      1.00000|

### Figure 1. Demand Curve and P<sub>MAX</sub> in Log-Log Space

<img src="plots/Figure_1-1.png" style="display: block; margin: auto;" />

### Figure 2. Model Slope and Modified Loss Function

<img src="plots/Figure_2-1.png" style="display: block; margin: auto;" />

### Figure 3. Box Plot and Unit Elasticity Distribution

<img src="plots/Figure_3-1.png" style="display: block; margin: auto;" />

### Figure 4. Comparison of Exact and Approximated P<sub>MAX</sub> Methods

<img src="plots/Figure_4-1.png" style="display: block; margin: auto;" />

### License

Copyright 2018, Shawn P. Gilroy (sgilroy1@lsu.edu)/Louisiana State University - GPLv3
