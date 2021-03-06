---
title       : My Child Height
subtitle    : You can predit your child height
author      : Aamarcha
job         : 
framework   : io2012        # {io2012, html5slides, shower, dzslides, ...}
highlighter : highlight.js  # {highlight.js, prettify, highlight}
hitheme     : tomorrow      # 
widgets     : []            # {mathjax, quiz, bootstrap}
mode        : selfcontained # {standalone, draft}
knit        : slidify::knit2slides
---

## Purposes

1. Predict the height of your child.
2. Plot the prediction within knowns data.

--- .class #methdology 

## Methodology
The fitted model used to predict child height :


```r
library(UsingR)
data(galton)
fitModel  <- lm(child ~., data=galton)
```
Then the child height is predicted using the model and the input height (for the parent).
For example:


```r
inputHeight  <- c(76)
predict(fitModel,newdata=data.frame(parent=inputHeight))
```

```
##     1 
## 73.06
```

--- .class #plotting
## Plotting
The predicted height of the child is shown within the galton data.

![plot of chunk plotting](assets/fig/plotting.png) 

--- .class #end
## Demo Time
1. Go to MyChildHeight app <a href="http://aamarcha.shinyapps.io/MyChildHeight/">MyChildHeight</a>
2. You can get the code on my Github repo <a href="https://github.com/aamarcha/mychildheight">MyChildHeight code</a>
3. Enjoy !
