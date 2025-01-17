


```r
library( dplyr )
library( knitr )
library( stringr )

GH.RAW <- "https://github.com/lecy/nccs/blob/main/catalogs/"
d <- read.csv( paste0( GH.RAW, "AWS-NCCSDATA.csv" ) )
source( paste0( GH.RAW, "build-catalog-functions.R" ) )
```



## CORE CATALOG


#### CHARITIES SCOPE PZ

```r
paths <- get_core_paths( paths=d$Key, tscope="CHARITIES", fscope="PZ" )
urls  <- make_urls( paths )
make_buttons( urls )


BUTTONS <- make_buttons( urls )
TSCOPE  <- get_core_tscope( paths )
FSCOPE  <- get_core_fscope( paths )
YEAR    <- get_core_year( paths )

catalog <- 
  data.frame( 
    BUTTONS, 
    NP_TYPE=TSCOPE, 
    FORM_SCOPE=FSCOPE, 
    YEAR=YEAR )

knitr::kable( catalog )
```

#### CHARITIES SCOPE PC

```r
paths <- get_core_paths( paths=d$Key, tscope="CHARITIES", fscope="PZ" )
urls  <- make_urls( paths )
make_buttons( urls )


BUTTONS <- make_buttons( urls )
TSCOPE  <- get_core_tscope( paths )
FSCOPE  <- get_core_fscope( paths )
YEAR    <- get_core_year( paths )

catalog <- 
  data.frame( 
    BUTTONS, 
    NP_TYPE=TSCOPE, 
    FORM_SCOPE=FSCOPE, 
    YEAR=YEAR )

knitr::kable( catalog )
```


#### NONPROFIT SCOPE PZ

```r
paths <- get_core_paths( paths=d$Key, tscope="NONPROFIT", fscope="PZ" )
urls  <- make_urls( paths )
make_buttons( urls )


BUTTONS <- make_buttons( urls )
TSCOPE  <- get_core_tscope( paths )
FSCOPE  <- get_core_fscope( paths )
YEAR    <- get_core_year( paths )

catalog <- 
  data.frame( 
    BUTTONS, 
    NP_TYPE=TSCOPE, 
    FORM_SCOPE=FSCOPE, 
    YEAR=YEAR )

knitr::kable( catalog )
```


#### NONPROFIT SCOPE PC

```r
paths <- get_core_paths( paths=d$Key, tscope="NONPROFIT", fscope="PC" )
urls  <- make_urls( paths )
make_buttons( urls )


BUTTONS <- make_buttons( urls )
TSCOPE  <- get_core_tscope( paths )
FSCOPE  <- get_core_fscope( paths )
YEAR    <- get_core_year( paths )

catalog <- 
  data.frame( 
    BUTTONS, 
    NP_TYPE=TSCOPE, 
    FORM_SCOPE=FSCOPE, 
    YEAR=YEAR )

knitr::kable( catalog )
```


#### FOUNDATIONS SCOPE PF

```r
paths <- get_core_paths( paths=d$Key, tscope="PRIVFOUND", fscope="PF" )
urls  <- make_urls( paths )
make_buttons( urls )


BUTTONS <- make_buttons( urls )
TSCOPE  <- get_core_tscope( paths )
FSCOPE  <- get_core_fscope( paths )
YEAR    <- get_core_year( paths )

catalog <- 
  data.frame( 
    BUTTONS, 
    NP_TYPE=TSCOPE, 
    FORM_SCOPE=FSCOPE, 
    YEAR=YEAR )

knitr::kable( catalog )

```


```
.button3 {
  background-color: #0a4c6a;
  color: white;
  border: 2px solid #0a4c6a;   
  text-align: center;
  text-decoration: none;
  display: inline-block;
  font-size: 14px;
  border-radius: 4px;
  width: 60px;
}
```