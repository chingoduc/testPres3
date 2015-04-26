My 3rd attempt
========================================================
author: Chi Ngo
date: Sun Apr 26 21:48:32 2015

First Slide
========================================================

For more details on authoring R presentations click the
**Help** button on the toolbar.

- Bullet 1
- Bullet 2
- Bullet 3

Slide With Code
========================================================


```r
summary(cars)
```

```
     speed           dist       
 Min.   : 4.0   Min.   :  2.00  
 1st Qu.:12.0   1st Qu.: 26.00  
 Median :15.0   Median : 36.00  
 Mean   :15.4   Mean   : 42.98  
 3rd Qu.:19.0   3rd Qu.: 56.00  
 Max.   :25.0   Max.   :120.00  
```

Slide With Plot
========================================================

![plot of chunk unnamed-chunk-2](testPres3-figure/unnamed-chunk-2-1.png) 
=============
### Introduction
- Basic tasks of data mining: data pre-processing, exploratory data analysis, and predictive model construction.
We are going to restrict our task to:
- look at two different ways to handle unknown values: by most frequent values and by similarity  and
- choose rtree as a way to create the prediction model of algaes provided by the dataset for predictions 
- Refer to my associated shiny application,  User will be allowed to select one of the seven algaes and the method to handle unknown values.
- In this report, we will only give an example about the case the "a1" algae
### Data Description
Data sets: Algae from the library "DMwR" of the book "Data Mining with R"
First data set has 200 samples, each contains 11 variables:
  - 3 nominal variables: (season, river size and river speed)
  - 8 values of different chemical parameters measured in the water samples: mxpH, mnO2, Cl, NO3, NH4, oPO4, PO4 and chlorophyll, and  
  - seven frequency of algae found in the respective water samples.

=============



### Methods

- Eliminate all samples which have more than 20% of the columns with an NA.


- Replacing all NAs using the most frequent value: The function centralImputation(), available in the library DMwR replaces all unknowns in a dataset by the median for numeric columns and the most frequent value for nominal variables.
- Modeling based on Regression Tree

![plot of chunk unnamed-chunk-5](testPres3-figure/unnamed-chunk-5-1.png) 

=============

- Replacing all NAs using the function knnImputation() in the library DMwR, k = 10 in our case.
- Modeling based on Regression Tree

![plot of chunk unnamed-chunk-6](testPres3-figure/unnamed-chunk-6-1.png) 

=============

### Conclusion

Not a big difference between the two Regression Tree for the prediction for the algae1 resulting form the two ways to replace the Unnown values

### Reference
Torgo, Luis.
Data mining with R : learning with case studies
ISBN 978-1-4398-1018-7 

