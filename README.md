Gender bias in ADHD diagnosis
================
Alexandra Rossy
(20 décembre, 2022)

- <a href="#introduction" id="toc-introduction">Introduction</a>
- <a href="#data-analyses" id="toc-data-analyses">Data analyses</a>
  - <a href="#data" id="toc-data">Data</a>
- <a href="#results" id="toc-results">Results</a>
- <a href="#conclusion" id="toc-conclusion">Conclusion</a>
- <a href="#references" id="toc-references">References</a>
  - <a href="#articles" id="toc-articles">Articles:</a>
  - <a href="#data-1" id="toc-data-1">Data:</a>
  - <a href="#picture" id="toc-picture">Picture:</a>

------------------------------------------------------------------------

![@ADHD_couple, instagram:
<https://www.instagram.com/p/CF7aB2NDL3j/?hl=fr>](ADHD_woman.jpg) \*\*\*

``` r
library(tidyverse)
```

    ## ── Attaching packages ─────────────────────────────────────── tidyverse 1.3.2 ──
    ## ✔ ggplot2 3.3.6      ✔ purrr   0.3.4 
    ## ✔ tibble  3.1.8      ✔ dplyr   1.0.10
    ## ✔ tidyr   1.2.1      ✔ stringr 1.4.1 
    ## ✔ readr   2.1.3      ✔ forcats 0.5.2 
    ## ── Conflicts ────────────────────────────────────────── tidyverse_conflicts() ──
    ## ✖ dplyr::filter() masks stats::filter()
    ## ✖ dplyr::lag()    masks stats::lag()

``` r
library(dplyr)
library(knitr)
library(ggplot2)
library("stringr")
library(shiny)
```

------------------------------------------------------------------------

## Introduction

ADHD is a neuro biological disorder characterized by attention deficit
and hyperactivity/impulsiveness (Purper-Ouakil *et al.*, 2011). People
can have this disorder with or without the hyperactivity. Indeed, the
symptoms are displayed on a spectrum (Heidbreder, 2015). Thus, the
diagnosis is not always easy to establish. ADHD is mostly present in
children but can persist into adulthood in 15 to 65% of cases (Katzman
*et al.*, 2017). Moreover, like for many deceases and disorders, the
research focused on white men for a long time. Therefore there still are
some miss or delayed diagnosis for some ethnical and social groups and
for women in general too (Dvorsky & Langberg, 2016). The main cause of
this gender bias diagnosis is the mentioned focus of the research on
symptoms typically shown on men, hence the recurrent delay in diagnose
of girls.

First of all, hormonal fluctuation in females may change the display of
the symptoms and thus they might not as salient as for men (Dvorsky &
Langberg, 2016). Then, symptoms for male are more externalized like
hyperactivity/impulsiveness (at least in childhood) whereas females tend
to be more inattentive (Quinn & Wigal, 2004) and their hyperactivity is
more internal with overt symptoms, such as displaying them in
hypertalkativeness way or emotional re-activity (Quinn, 2005).
Therefore, their symptoms are less noticeable than males ones (Katzman
*et al.*, 2017). Moreover, with a late diagnosis, females also have more
time to developed coping strategies making the diagnosis even more
difficult to establish (Katzman *et al.*, 2017). In addition, linked
with hormonal fluctuations and commodities resulting from a delayed
diagnosis, such as chronic anxiety, mood disorder etc., females are
often blurring medical examination and tend to be firstly diagnosed with
depression or other mood disorder (Quinn, 2005). Finally, society has
also a role in this bias, indeed, girls are being told since childhood
to internalized negative feedback, to accommodate, to be quiet and calm
etc. Men, on the other hand, are being encouraged to be open, dynamic
and to take opportunities etc.(Quinn, 2005). As a matter of fact, as I
said before, girls will developed coping strategies and internalized
their hyperactivity and increase the risk to develop anxiety, low
self-esteem etc. (Quinn, 2005).

Apart from the lack of research on women, it seems that boys have a 2 to
2.5 higher prevalence of ADHD than girls (Dvorsky & Langberg, 2016).
However, I feel like those numbers are difficult to estimate because
ADHD is becoming more and more well-known, we see an increasing number
of diagnoses among the world and maybe with the research on females
being on the rise too, the average of people with ADHD might be even
higher than we think.

------------------------------------------------------------------------

## Data analyses

Since girls are often miss- and mis- diagnosed, and when they are, the
diagnosis is often delayed, my hypothesis is the following:

→ **“The difference between children and adult women with ADHD is lower
than the difference between children and adult men with ADHD.”**

As previously mentioned, 15-65% of children will still have ADHD while
growing up. If we take into account that some girls might have delayed
diagnoses, often only at adulthood, the difference between the girls’
and the women rate will be smaller. Regarding the boys’ and the men
rate, boys are more likely to be diagnosed as childs and thus the
percentage of grown up men with ADHD will follow the trend of 15 to 65%
of children diagnosed who will still have ADHD while growing up.

### Data

First of all, I was interested in confirming whether boys with ADHD were
more numerous than girls. I took my
[data](https://www.childhealthdata.org/browse/survey/allstates?q=9343&g=1008&a=18062#)
from the *National Survey of Children’s Health* of the USA, from a
2020-2021 survey. The data identify children age ranging from 3 to 17
years old from each states of the USA with a current diagnosis of ADHD.

**The table looks like this:**

``` r
children <- readxl::read_xlsx("children_gender.xlsx")
my_table <- (head(children))

my_table %>% kable()  
```

| State   | Gender | ADHD |
|:--------|:-------|-----:|
| Alabama | M      | 16.2 |
| ALabama | F      | 11.1 |
| Alaska  | M      |  7.3 |
| Alaska  | F      |  4.3 |
| Arizona | M      | 11.3 |
| Arizona | F      |  6.0 |

``` r
#For further information about my data

summary(children)
```

    ##     State              Gender               ADHD       
    ##  Length:102         Length:102         Min.   : 3.100  
    ##  Class :character   Class :character   1st Qu.: 6.225  
    ##  Mode  :character   Mode  :character   Median : 9.350  
    ##                                        Mean   : 9.835  
    ##                                        3rd Qu.:13.075  
    ##                                        Max.   :22.200

``` r
children %>% kable()
```

| State                | Gender | ADHD |
|:---------------------|:-------|-----:|
| Alabama              | M      | 16.2 |
| ALabama              | F      | 11.1 |
| Alaska               | M      |  7.3 |
| Alaska               | F      |  4.3 |
| Arizona              | M      | 11.3 |
| Arizona              | F      |  6.0 |
| Arkansas             | M      | 17.4 |
| Arkansas             | F      |  9.8 |
| California           | M      |  6.2 |
| California           | F      |  3.1 |
| Colorado             | M      | 10.2 |
| Colorado             | F      |  6.1 |
| Connecticut          | M      | 13.2 |
| Connecticut          | F      |  3.2 |
| Delaware             | M      | 10.8 |
| Delaware             | F      |  7.5 |
| District of Columbia | M      | 11.5 |
| District of Columbia | F      |  3.2 |
| Florida              | M      | 16.9 |
| Florida              | F      |  7.8 |
| Georgia              | M      | 14.1 |
| Georgia              | F      |  6.4 |
| Hawaii               | M      |  8.0 |
| Hawaii               | F      |  3.7 |
| Idaho                | M      | 11.1 |
| Idaho                | F      |  6.1 |
| Illinois             | M      |  9.9 |
| Illinois             | F      |  3.8 |
| Indiana              | M      | 17.5 |
| Indiana              | F      | 10.4 |
| Iowa                 | M      | 13.1 |
| Iowa                 | F      |  6.4 |
| Kansas               | M      | 11.8 |
| Kansas               | F      |  5.8 |
| Kentucky             | M      | 15.5 |
| Kentucky             | F      | 10.1 |
| Louisiana            | M      | 22.2 |
| Louisiana            | F      |  9.2 |
| Maine                | M      | 17.7 |
| Maine                | F      |  7.2 |
| Maryland             | M      | 11.9 |
| Maryland             | F      |  6.4 |
| Massachusetts        | M      | 13.3 |
| Massachusetts        | F      |  6.9 |
| Michigan             | M      | 14.5 |
| Michigan             | F      |  6.3 |
| Minnesota            | M      |  7.5 |
| Minnesota            | F      |  6.2 |
| Mississippi          | M      | 17.7 |
| Mississippi          | F      | 10.6 |
| Missouri             | M      | 12.0 |
| Missouri             | F      |  5.5 |
| Montana              | M      | 14.1 |
| Montana              | F      |  4.2 |
| Nebraska             | M      | 10.5 |
| Nebraska             | F      |  4.8 |
| Nevada               | M      |  6.6 |
| Nevada               | F      |  4.9 |
| New Hampshire        | M      | 17.9 |
| New Hampshire        | F      |  8.3 |
| New Jersey           | M      |  9.5 |
| New Jersey           | F      |  5.7 |
| New Mexico           | M      | 12.7 |
| New Mexico           | F      |  6.5 |
| New York             | M      | 11.8 |
| New York             | F      |  3.4 |
| North Carolina       | M      | 16.4 |
| North Carolina       | F      |  9.0 |
| North Dakota         | M      | 12.5 |
| North Dakota         | F      |  6.2 |
| Ohio                 | M      | 15.3 |
| Ohio                 | F      |  6.8 |
| Oklahoma             | M      | 11.4 |
| Oklahoma             | F      |  8.2 |
| Oregon               | M      | 12.1 |
| Oregon               | F      |  5.2 |
| Pennsylvania         | M      | 14.5 |
| Pennsylvania         | F      |  4.5 |
| Rhode Island         | M      | 16.1 |
| Rhode Island         | F      |  5.3 |
| South Carolina       | M      | 17.3 |
| South Carolina       | F      |  9.5 |
| South Dakota         | M      | 11.3 |
| South Dakota         | F      |  8.1 |
| Tennessee            | M      | 14.1 |
| Tennessee            | F      |  7.7 |
| Texas                | M      | 13.0 |
| Texas                | F      |  7.4 |
| Utah                 | M      |  8.6 |
| Utah                 | F      |  4.4 |
| Vermont              | M      | 13.2 |
| Vermont              | F      |  9.1 |
| Virginia             | M      | 15.2 |
| Virginia             | F      |  8.3 |
| Washington           | M      | 13.3 |
| Washington           | F      |  5.6 |
| West Virginia        | M      | 16.8 |
| West Virginia        | F      |  7.9 |
| Wisconsin            | M      | 10.8 |
| Wisconsin            | F      |  5.1 |
| Wyoming              | M      | 15.6 |
| Wyoming              | F      |  4.6 |

**→** **Therefore I decided to do a boxplot to confirm the expected
results:**

``` r
ggplot(children, aes(x= Gender, y= ADHD, fill=Gender))+
  geom_boxplot()+
  ggtitle("Percentage of children with ADHD in the USA")+
  theme(plot.title = element_text(hjust=0.5) )
```

![](datapractical_files/figure-gfm/unnamed-chunk-4-1.png)<!-- -->

``` r
girls <- children %>% filter(Gender=="F") %>% filter(ADHD=TRUE)


boys <- children %>% filter(Gender=="M") %>% filter(ADHD=TRUE)


mean_boys <- mean(boys$ADHD)


mean_girls <- mean(girls$ADHD)


children_tab <- data.frame("Girls" =mean_girls, "Boys" = mean_boys)

test_children <- t.test(girls$ADHD, boys$ADHD)


#results: t = -11.872, df = 83.933, p-value < 2.2e-16
#significant difference between boys and girls 
```

As we can see on the boxplot, and after realizing a t.test, the average
of boys with ADHD is significantly higher than the average of girls
(p-value \< 0,05).

Then, I took data about the mean percentage of adults in the USA with
ADHD. [My
data](https://www.nimh.nih.gov/health/statistics/attention-deficit-hyperactivity-disorder-adhd#part_2553)
come from the *National Institute of Mental Health*. Unfortunately, the
most recent data I could find for the USA are from 2006.

- **I decided to build a barplot in order to compare the mean for men
  and for women adults:**

``` r
library(gridExtra)

adult <- readxl::read_xlsx("adult_adhd.xlsx")

mean_adult <- data.frame("Women"= 3.2, "Men"= 5.4)


ggplot(adult, aes(x= Gender, y= Percentage, fill=Gender))+
  geom_bar(stat="identity", width = 0.5)+
  ggtitle("Average of adult with ADHD in the USA")+
  theme(plot.title = element_text(hjust=0.5))+
  ylim(0,15)
```

![](datapractical_files/figure-gfm/unnamed-chunk-5-1.png)<!-- -->

``` r
plot1 <- ggplot(adult, aes(x= Gender, y= Percentage, fill=Gender))+
  geom_bar(stat="identity", width = 0.5)+
  ylim(0,15)+
  theme(legend.position ="none")+
  xlab("Adults")

mean_adult %>% kable(caption="Percentage of adult with ADHD in the USA")
```

| Women | Men |
|------:|----:|
|   3.2 | 5.4 |

Percentage of adult with ADHD in the USA

``` r
test_adult <- t.test(mean_adult)


#results: t = 3.9091, df = 1, p-value = 0.1594
#seems to be no significant difference between men and women --> so something must have changed between adult and children. seems to go in the direction of my hypothesis. 
```

This time, the t.test I realized showed no significant difference
between the men and the women percentage with ADHD. This change of
significance may go in the direction of my hypothesis ( p-value =
0.1594).

``` r
children_mean <- readxl::read_xlsx("children_mean.xlsx")
female_tab <- readxl::read_xlsx("female_tab.xlsx")
male_tab <- readxl::read_xlsx("male_tab.xlsx")



ggplot(children_mean, aes(x=Gender, y=Percentage, fill=Gender))+
  geom_bar(stat="identity", width = 0.5)+
  ggtitle("Average of children with ADHD in the USA")+
  theme(plot.title = element_text(hjust=0.5))+
  ylim(0,15)
```

![](datapractical_files/figure-gfm/unnamed-chunk-6-1.png)<!-- -->

``` r
children_tab %>% kable(caption = " Average percentage of children with ADHD in the USA")
```

|    Girls |     Boys |
|---------:|---------:|
| 6.545098 | 13.12549 |

Average percentage of children with ADHD in the USA

``` r
plot2 <- ggplot(children_mean, aes(x=Gender, y=Percentage, fill=Gender))+
  geom_bar(stat="identity", width = 0.5)+
  ylim(0,15)+
  theme(legend.position="none")+
  xlab("Children")
```

- **In order to have a better visualization of mean percentage for
  children with ADHD compared to adults with ADHD, I decided to group
  the barplots.**

``` r
grid.arrange(plot1,plot2, ncol=2, top="Average population with ADHD in the USA")
```

![](datapractical_files/figure-gfm/unnamed-chunk-7-1.png)<!-- -->

``` r
female_plot <- ggplot(female_tab, aes(x=Gender, y=Percentage))+
  geom_bar(stat="identity", width = 0.5, fill="coral1")+
  ylim(0,15)+
  theme(legend.position="none")+
  xlab("Female")
  

male_plot <- ggplot(male_tab, aes(x=Gender, y=Percentage))+
   geom_bar(stat="identity", width = 0.5, fill="darkturquoise")+
  ylim(0,15)+
  theme(legend.position="none")+
  xlab("Male")

grid.arrange(female_plot,male_plot, ncol=2, top="Difference between children and adults")
```

![](datapractical_files/figure-gfm/unnamed-chunk-7-2.png)<!-- -->

``` r
both <- matrix(c(3.2,5.4,6.55,13.13), ncol=4, byrow=TRUE)

colnames(both)= c("Female","Male","Girls","Boys")

both %>% kable(caption="Average population with ADHD")
```

| Female | Male | Girls |  Boys |
|-------:|-----:|------:|------:|
|    3.2 |  5.4 |  6.55 | 13.13 |

Average population with ADHD

``` r
percent <- matrix(c("~ 49%", "~ 43%"), ncol=2, byrow=TRUE)
colnames(percent)= c("Women","Men")

percent %>% kable(caption="Percentage of adults who still have ADHD")  
```

| Women  | Men    |
|:-------|:-------|
| \~ 49% | \~ 43% |

Percentage of adults who still have ADHD

``` r
results <- t.test(male_tab$Percentage,female_tab$Percentage, var.equal = FALSE)
results
```

    ## 
    ##  Welch Two Sample t-test
    ## 
    ## data:  male_tab$Percentage and female_tab$Percentage
    ## t = 1.0422, df = 1.3628, p-value = 0.4473
    ## alternative hypothesis: true difference in means is not equal to 0
    ## 95 percent confidence interval:
    ##  -24.85411  33.63411
    ## sample estimates:
    ## mean of x mean of y 
    ##     9.265     4.875

``` r
#results: t = 1.0422, df = 1.3628, p-value = 0.4473
#as the significance value alpha = 0.05, p-value is > and so there is no significance difference between F and M, ADHD.   
```

As I said previously, it is estimated that 15 to 65 % of children will
still have ADHD while growing up.  
On the last table, we can see that we still have an average of 49% of
6.55 % of girls who still have ADHD while growing up. For the men we
have a bit less than this average, since around 43% of the 13.13% of
boys with ADHD will still have the disorder as an adult. I also realized
a t.test which showed no significance for this difference of percentage
between male and female (p-value = 0.4473). Both 43% and 49% are in the
expected results of children who would keep the disorder in adulthood.

------------------------------------------------------------------------

## Results

- **If we recap:**

``` r
test_table <- matrix(c("p-value < 2.2e-16", "p-value = 0.1594","p-value = 0.4473"), ncol=3, byrow = TRUE)
colnames(test_table)= c("For children", "For adults", "For children vs adults")

test_table %>%kable(caption="T.test for significance")
```

| For children       | For adults       | For children vs adults |
|:-------------------|:-----------------|:-----------------------|
| p-value \< 2.2e-16 | p-value = 0.1594 | p-value = 0.4473       |

T.test for significance

There is only one significant difference for the percentage of boys and
girls diagnosed with ADHD. The fact that there isn’t significant
difference among adult might go on the same direction as my hypothesis.
Moreover, the higher percentage of girls who might keep ADHD while
growing up comparing to the one for boys slightly supports my
hypothesis. However, my hypothesis is not supported in a very reliable
way as there is no significant difference between these two percentages.

Furthermore, I couldn’t find data for both adults and children from the
same year of survey and the research about ADHD are increasing such as
awareness. Therefore, my results aren’t very reliable since I might not
be comparing the same proportion of percentage in the actual population.

------------------------------------------------------------------------

## Conclusion

As I said previously, my results aren’t very reliable. However, it seems
that girls still have a higher rate of delayed diagnosis which can be
very impactful in their life. Actually, an early diagnosis in childhood
allows for the development of a treatment plan and strategies to deal
with everything that ADHD entails (for example organization problem,
focus, school tasks etc.). As a matter of facts, an undiagnosed and not
treated ADHD increase the risk of developing comorbidities such as
anxiety, psychological distress, depression and low self-esteem (Quinn,
2005). It also often leads to social relationship impairs,
school/working failure, general demoralization and increase the risk of
consuming drugs or alcohol (Quinn, 2005). This not only impacts women
but also threatens public health. Indeed, untreated/undiagnosed women
tend to be less able to be consistent parents and less able to manage
their job and private life. In addition, the anxiety and stress
resulting from all these struggles can cause several important deceases
(Quinn, 2005).

For all the reasons I have mentioned in this paper, awareness about ADHD
is very important in order to increase the number of diagnoses and not
to forget anyone that could suffer in silence. Finally, as Dvorksy and
Langberg (2016) suggest, “it may be preferable to ensure that (a)
diagnostic items reflect both male- and female-specific manifestations,
(b) subtle indicators of inattention/disorganization are probed, and (c)
clinicians inquire about such factors as compensatory behaviors and life
transitions in girls and women.”

------------------------------------------------------------------------

## References

### Articles:

Dvorsky, M.R., Langberg, J.M. (2016). A Review of Factors that Promote
Resilience in Youth with ADHD and ADHD Symptoms. *Clin Child Fam Psychol
Rev* 19, 368–391.

Heidbreder R. (2015). ADHD symptomatology is best conceptualized as a
spectrum: a dimensional versus unitary approach to diagnosis. *Attention
deficit and hyperactivity disorders*, 7(4), 249–269.

Katzman, M.A., Bilkey, T.S., Chokka, P.R. *et al.* (2017). Adult ADHD
and comorbid disorders: clinical implications of a dimensional approach.
*BMC Psychiatry* 17, 302.

Purper-Ouakil, D., Ramoz, N., Lepagnol-Bestel, AM. *et al.* (2011).
Neurobiology of Attention Deficit/Hyperactivity Disorder. *Pediatr Res*
69, 69–76.

Quinn, P., Wigal, S. (2004). Perceptions of girls and ADHD: results from
a national survey. *MedGenMed* 6(2):2.

Quinn, P.O. (2005). Treating adolescent girls and women with ADHD:
Gender-Specific issues. *J. Clin. Psychol.*, 61: 579-587.

### Data:

- National Institute of Mental Health, from:
  - Kessler, R. C., Adler, L., Barkley, R., Biederman, J., Conners, C.
    K., Demler, O., Faraone, S. V., Greenhill, L. L., Howes, M. J.,
    Secnik, K., Spencer, T., Ustun, T. B., Walters, E. E., &
    Zaslavsky, A. M. (2006). The prevalence and correlates of adult ADHD
    in the United States: results from the National Comorbidity Survey
    Replication. *The American journal of psychiatry*, 163(4), 716–723.
    - [Data
      table](https://www.nimh.nih.gov/health/statistics/attention-deficit-hyperactivity-disorder-adhd#part_2553)
- Child and Adolescent Health Measurement Initiative. 2020-2021 National
  Survey of Children’s Health (NSCH) data query. Data Resource Center
  for Child and Adolescent Health supported by the U.S. Department of
  Health and Human Services, Health Resources and Services
  Administration (HRSA), Maternal and Child Health Bureau (MCHB).
  Retrieved from <https://mchb.hrsa.gov/data/national-surveys>
  - [Data
    table](https://www.childhealthdata.org/browse/survey/allstates?q=9343&g=1008&a=18062#)

### Picture:

- \[@ADHD_couple\].(2020, October 4).Retrieved on
  [Instagram](https://www.instagram.com/p/CF7aB2NDL3j/?hl=f)
