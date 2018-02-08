---
title: "xe"
output: 
  html_document: 
    keep_md: yes
---


```r
knitr::opts_chunk$set(echo = TRUE, eval = FALSE)
```

Communicating with hafvog

Installing:


```r
devtools::install_github("fishvice/xe",  dependencies = FALSE, args='--no-multiarch')
```


```r
con <- connect_xe(user = "xxxx")
```

and then buisness as usual:


```r
library(mar)
library(xe)
lesa_stodvar(con)
lesa_lengdir(con)
lesa_kvarnir(con)
lesa_numer(con)
```





