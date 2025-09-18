Data Manipulation
================

``` r
library(tidyverse)
```

Import data

``` r
litters_df = read_csv(
  file = "./data/FAS_litters.csv",
  na = c(".", "NA", ""))
```

    ## Rows: 49 Columns: 8
    ## ── Column specification ────────────────────────────────────────────────────────
    ## Delimiter: ","
    ## chr (2): Group, Litter Number
    ## dbl (6): GD0 weight, GD18 weight, GD of Birth, Pups born alive, Pups dead @ ...
    ## 
    ## ℹ Use `spec()` to retrieve the full column specification for this data.
    ## ℹ Specify the column types or set `show_col_types = FALSE` to quiet this message.

``` r
litters_df = 
  janitor::clean_names(litters_df)

pups_df = read_csv(
  file ="./data/FAS_litters.csv",
  skip  = 3,
  na = c(".", "NA", ""))
```

    ## Rows: 46 Columns: 8
    ## ── Column specification ────────────────────────────────────────────────────────
    ## Delimiter: ","
    ## chr (2): Con7, #5/5/3/83/3-3
    ## dbl (6): 26, 41.4, 19, 6, 0, 5
    ## 
    ## ℹ Use `spec()` to retrieve the full column specification for this data.
    ## ℹ Specify the column types or set `show_col_types = FALSE` to quiet this message.

``` r
pups_df =
  janitor::clean_names(pups_df)

#skimr::skim(litters_df)
```
