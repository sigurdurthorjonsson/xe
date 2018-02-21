---
title: "xe"
output: 
  html_document: 
    keep_md: yes
---



Communicating with hafvog

Installing:


```r
devtools::install_github("fishvice/xe",  dependencies = FALSE, args='--no-multiarch')
```

connection to the xe would be:


```r
library(lubridate)
library(tidyverse)

library(xe)
con <- connect_xe(user = "xxxx")
```

and then buisness as usual:

```r
lesa_stodvar(con)
lesa_lengdir(con)
lesa_kvarnir(con)
lesa_numer(con)
```

Gathering all smb data into R can be done via:

```r
read_smx_data(con, Leidangur = "TB1-2017", year.now = 2017)  # last two arguments a temporary fix
save(st, st.done, stadlar_lw, stadlar_rallstodvar, stadlar_tegundir,
     fisktegundir, le, kv, nu, file = "smb.rda")
```

Update also these libraries if you want to use the SMB dashboard:

```r
install.packages("shiny")
install.packages("leaflet")
install.packages("flexdashboard")
```



