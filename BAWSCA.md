BAWSCA
================
RPrice
2/12/2021

``` r
#must have Java and JavaJDK installed
Sys.setenv(JAVA_HOME="C:/Program Files/Java/jdk-15.0.2/")
library(rJava)
library(tabulizer); library(tabulizerjars)
```

``` r
f <- "BAWSCA_AnnualSurvey18-19.pdf"
tab <- tabulizer::extract_tables(f,pages = 24)
head(tab[[1]])
```

    ##      [,1]                                            [,2]        
    ## [1,] ""                                              ""          
    ## [2,] ""                                              "Service"   
    ## [3,] ""                                              "Population"
    ## [4,] "San Mateo County"                              ""          
    ## [5,] "City of Brisbane / Guadalupe Valley Municipal" ""          
    ## [6,] "Improvement District"                          "4,587"     
    ##      [,3]               
    ## [1,] "Water Purchased /"
    ## [2,] "Produced (mgd)"   
    ## [3,] "SF RWS* Total"    
    ## [4,] ""                 
    ## [5,] ""                 
    ## [6,] "0.66 0.66"        
    ##      [,4]                                                                            
    ## [1,] ""                                                                              
    ## [2,] ""                                                                              
    ## [3,] "Communities Served (all or portions of)"                                       
    ## [4,] ""                                                                              
    ## [5,] "Brisbane, nearby unincorporated areas, and GVMID, an industrial park and small"
    ## [6,] "residential community within the City of Brisbane"

``` r
tab <- tabulizer::extract_tables(f,pages = 28)
```
