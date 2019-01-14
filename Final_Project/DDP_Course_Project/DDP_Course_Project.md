Developing Data Products Course Project
========================================================
author: James Francisco
date: Jan. 12, 2019
autosize: true



Introduction
========================================================
This presentation and the associated shiny app conclude the Coursera course: Developing Data products. 

Included in this project are:

- this presentation, providing an overview, code examples and links
- a shiny app hosted on shinyapp.io
- the corresponding source code hosted via github

Description of the app
========================================================

This app has been developed for the Developing Data Products Course, from Coursera. This app helps a user to choose a car for daily commuting, using the mtcars dataset from [R]. The mtcars data set is somewhat stale. To make this app useful for drivers now, a data frame with data for current cars would need to be built. 


Mutating Data
========================================================

In order to facilitate sorting, the values for the transmission field in the data was transformed from 'automatic' and 'manual' to '0' and '1'.


```r
data <- mutate(mtcars, am = ifelse(am=="Automatic", 0, 1))
head(data)
```

```
   mpg cyl disp  hp drat    wt  qsec vs am gear carb
1 21.0   6  160 110 3.90 2.620 16.46  0  1    4    4
2 21.0   6  160 110 3.90 2.875 17.02  0  1    4    4
3 22.8   4  108  93 3.85 2.320 18.61  1  1    4    1
4 21.4   6  258 110 3.08 3.215 19.44  1  1    3    1
5 18.7   8  360 175 3.15 3.440 17.02  0  1    3    2
6 18.1   6  225 105 2.76 3.460 20.22  1  1    3    1
```

MPG Comparisons
========================================================

![plot of chunk unnamed-chunk-3](DDP_Course_Project-figure/unnamed-chunk-3-1.png)

Graphical comparisons can be created for the parameters in the application to show the effects on performance from the car's characteristics.
***
![plot of chunk unnamed-chunk-4](DDP_Course_Project-figure/unnamed-chunk-4-1.png)

