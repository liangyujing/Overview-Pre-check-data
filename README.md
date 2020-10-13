```{r}
#check normality of predictor vaiables
library(car)
library(qualityTools)

#histogram to see how RMSSD is skewed
hist(mixedef_correct_incorrect$baseline_RMSSD,probability=T, main="Histogram of distributed RMSSD
     data",xlab="distributed RMSSD data")
lines(density(mixedef_correct_incorrect$baseline_RMSSD),col=2)

#qqplot RT
qqPlot(mixedef_correct_incorrect$baseline_RMSSD)
#not normal distributed what is to be expected based on the literature, right skewed

#histogram to see how RT is skewed
hist(mixedef_correct_incorrect$RT,probability=T, main="Histogram of distributed RT
     data",xlab="distributed RT data")
lines(density(mixedef_correct_incorrect$RT),col=2)

#qqplot RT
qqPlot(mixedef_correct_incorrect$RT)
#It is right skewed

#histogram to see how confidence is skewed
hist(mixedef_correct_incorrect$confidence,probability=T, main="Histogram of distributed confidence data",
     xlab="distributed confidence data")
lines(density(mixedef_correct_incorrect$confidence),col=2)

#qqplot RT
qqPlot(mixedef_correct_incorrect$confidence)
#It is left skewed
```
