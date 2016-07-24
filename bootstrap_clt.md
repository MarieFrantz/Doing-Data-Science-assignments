# bootstrap assignment 4
Marie Wallmark  
May 31, 2016  
#this is to illustrate the Central limit theorem in R markdown:

```r
n<-30
nsim<-1000
bootnorm<-numeric(nsim)
for (i in 1:nsim){
  x<-rnorm(n)
  bootnorm [i]<-median(x)
}
summary(bootnorm)
```

```
##      Min.   1st Qu.    Median      Mean   3rd Qu.      Max. 
## -0.704200 -0.158600 -0.013380 -0.007687  0.138300  0.816800
```

```r
hist(bootnorm)
```

![](bootstrap_clt_files/figure-html/unnamed-chunk-1-1.png)<!-- -->

```r
sd (x)
```

```
## [1] 0.8878663
```

```r
#using a second sample size
n<-60
nsim<-1000
bootnorm<-numeric(nsim)
for (i in 1:nsim){
  x<-rnorm(n)
  bootnorm [i]<-median(x)
}
summary(bootnorm)
```

```
##      Min.   1st Qu.    Median      Mean   3rd Qu.      Max. 
## -0.464700 -0.100100  0.006235  0.004269  0.106300  0.482700
```

```r
hist(bootnorm)
```

![](bootstrap_clt_files/figure-html/unnamed-chunk-1-2.png)<!-- -->

```r
sd (x)
```

```
## [1] 0.9658474
```

```r
#exponential distribution
n<-rexp(1000,1/50)
```
