Gender bias in ADHD diagnosis
================
Alexandra Rossy
(07 décembre, 2022)

![@ADHD_couple, instagram:
<https://www.instagram.com/p/CF7aB2NDL3j/?hl=fr>](/Users/alex-/Master/data%20sciences/datapractical/ADHD_woman.jpg)

## Introduction

- fact
- fact

## References

### Articles:

Hinshaw, S. P., Nguyen, P. T., O’Grady, S. M., & Rosenthal, E. A.
(2022). Annual Research Review: Attention-deficit/hyperactivity disorder
in girls and women: underrepresentation, longitudinal processes, and key
directions. *Journal of child psychology and psychiatry, and allied
disciplines*, 63(4), 484–496.

Slobodin, O. & Davidovitch, M.(2019). Gender Differences in Objective
and Subjective Measures of ADHD Among Clinic-Referred Children.
*Frontiers*.

### Data:

- National Survey of Children’s Health, Health Resources and Services
  Administration, Maternal and Child Health Bureau.
  <https://mchb.hrsa.gov/data/national-surveys>
  - [Data
    table](https://www.childhealthdata.org/browse/survey/allstates?q=9343&g=1008&a=18062#)

### Pictures:

- @ADHD_couple on
  [Instagram](https://www.instagram.com/p/CF7aB2NDL3j/?hl=f)

<!-- -->

    ## ── Attaching packages ─────────────────────────────────────── tidyverse 1.3.2 ──
    ## ✔ ggplot2 3.3.6      ✔ purrr   0.3.4 
    ## ✔ tibble  3.1.8      ✔ dplyr   1.0.10
    ## ✔ tidyr   1.2.1      ✔ stringr 1.4.1 
    ## ✔ readr   2.1.3      ✔ forcats 0.5.2 
    ## ── Conflicts ────────────────────────────────────────── tidyverse_conflicts() ──
    ## ✖ dplyr::filter() masks stats::filter()
    ## ✖ dplyr::lag()    masks stats::lag()
    ## New names:

    ## # A tibble: 51 × 4
    ##     ...1 State                `Male %` `Female %`
    ##    <dbl> <chr>                   <dbl>      <dbl>
    ##  1     1 Alabama                  16.2       11.1
    ##  2     2 Alaska                    7.3        4.3
    ##  3     3 Arizona                  11.3        6  
    ##  4     4 Arkansas                 17.4        9.8
    ##  5     5 California                6.2        3.1
    ##  6     6 Colorado                 10.2        6.1
    ##  7     7 Connecticut              13.2        3.2
    ##  8     8 Delaware                 10.8        7.5
    ##  9     9 District of Columbia     11.5        3.2
    ## 10    10 Florida                  16.9        7.8
    ## # … with 41 more rows

    ## New names:
    ## • `` -> `...1`

    ##       ...1         State               Male %         Female %     
    ##  Min.   : 1.0   Length:51          Min.   : 6.20   Min.   : 3.100  
    ##  1st Qu.:13.5   Class :character   1st Qu.:11.20   1st Qu.: 5.000  
    ##  Median :26.0   Mode  :character   Median :13.10   Median : 6.300  
    ##  Mean   :26.0                      Mean   :13.13   Mean   : 6.545  
    ##  3rd Qu.:38.5                      3rd Qu.:15.55   3rd Qu.: 8.000  
    ##  Max.   :51.0                      Max.   :22.20   Max.   :11.100

    ## [1] 6.545098

    ## [1] 13.13137

    ## tibble [51 × 1] (S3: tbl_df/tbl/data.frame)
    ##  $ Male %: num [1:51] 16.2 7.3 11.3 17.4 6.2 10.2 13.2 10.8 11.5 16.9 ...

    ## tibble [51 × 1] (S3: tbl_df/tbl/data.frame)
    ##  $ Female %: num [1:51] 11.1 4.3 6 9.8 3.1 6.1 3.2 7.5 3.2 7.8 ...

|  …1 | State                | Male % | Female % |
|----:|:---------------------|-------:|---------:|
|   1 | Alabama              |   16.2 |     11.1 |
|   2 | Alaska               |    7.3 |      4.3 |
|   3 | Arizona              |   11.3 |      6.0 |
|   4 | Arkansas             |   17.4 |      9.8 |
|   5 | California           |    6.2 |      3.1 |
|   6 | Colorado             |   10.2 |      6.1 |
|   7 | Connecticut          |   13.2 |      3.2 |
|   8 | Delaware             |   10.8 |      7.5 |
|   9 | District of Columbia |   11.5 |      3.2 |
|  10 | Florida              |   16.9 |      7.8 |
|  11 | Georgia              |   14.4 |      6.4 |
|  12 | Hawaii               |    8.0 |      3.7 |
|  13 | Idaho                |   11.1 |      6.1 |
|  14 | Illinois             |    9.9 |      3.8 |
|  15 | Indiana              |   17.5 |     10.4 |
|  16 | Iowa                 |   13.1 |      6.4 |
|  17 | Kansas               |   11.8 |      5.8 |
|  18 | Kentucky             |   15.5 |     10.1 |
|  19 | Louisiana            |   22.2 |      9.2 |
|  20 | Maine                |   17.7 |      7.2 |
|  21 | Maryland             |   11.9 |      6.4 |
|  22 | Massachusetts        |   13.3 |      6.9 |
|  23 | Michigan             |   14.5 |      6.3 |
|  24 | Minnesota            |    7.5 |      6.2 |
|  25 | Mississippi          |   17.7 |     10.6 |
|  26 | Missouri             |   12.0 |      5.5 |
|  27 | Montana              |   14.1 |      4.2 |
|  28 | Nebraska             |   10.5 |      4.8 |
|  29 | Nevada               |    6.6 |      4.9 |
|  30 | New Hampshire        |   17.9 |      8.3 |
|  31 | New Jersey           |    9.5 |      5.7 |
|  32 | New Mexico           |   12.7 |      6.5 |
|  33 | New York             |   11.8 |      3.4 |
|  34 | North Carolina       |   16.4 |      9.0 |
|  35 | North Dakota         |   12.5 |      6.2 |
|  36 | Ohio                 |   15.3 |      6.8 |
|  37 | Oklahoma             |   11.4 |      8.2 |
|  38 | Oregon               |   12.1 |      5.2 |
|  39 | Pennsylvania         |   14.5 |      4.5 |
|  40 | Rhode Island         |   16.1 |      5.3 |
|  41 | South Carolina       |   17.3 |      9.5 |
|  42 | South Dakota         |   11.3 |      8.1 |
|  43 | Tennessee            |   14.1 |      7.7 |
|  44 | Texas                |   13.0 |      7.4 |
|  45 | Utah                 |    8.6 |      4.4 |
|  46 | Vermont              |   13.2 |      9.1 |
|  47 | Virginia             |   15.2 |      8.3 |
|  48 | Washington           |   13.3 |      5.6 |
|  49 | West Virginia        |   16.8 |      7.9 |
|  50 | Wisconsin            |   10.8 |      5.1 |
|  51 | Wyoming              |   15.6 |      4.6 |

|    Girls |     Boys |
|---------:|---------:|
| 6.545098 | 13.13137 |

![](datapractical_files/figure-gfm/unnamed-chunk-1-1.png)<!-- -->
