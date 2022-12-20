Gender bias in ADHD diagnosis
================
Alexandra Rossy
(19 décembre, 2022)

![@ADHD_couple, instagram:
<https://www.instagram.com/p/CF7aB2NDL3j/?hl=fr>](ADHD_woman.jpg)

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

| State   | Gender | ADHD |
|:--------|:-------|-----:|
| Alabama | M      | 16.2 |
| ALabama | F      | 11.1 |
| Alaska  | M      |  7.3 |
| Alaska  | F      |  4.3 |
| Arizona | M      | 11.3 |
| Arizona | F      |  6.0 |

**→** **Therefore I decided to do a boxplot to confirm the expected
results:**

![](datapractical_files/figure-gfm/unnamed-chunk-4-1.png)<!-- -->

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

![](datapractical_files/figure-gfm/unnamed-chunk-5-1.png)<!-- -->

| Women | Men |
|------:|----:|
|   3.2 | 5.4 |

Percentage of adult with ADHD in the USA

This time, the t.test I realized showed no significant difference
between the men and the women percentage with ADHD. This change of
significance may go in the direction of my hypothesis ( p-value =
0.1594).

- **In order to have a better visualization of mean percentage for
  children with ADHD compared to adults with ADHD, I decided to group
  the barplots.**

![](datapractical_files/figure-gfm/unnamed-chunk-7-1.png)<!-- -->![](datapractical_files/figure-gfm/unnamed-chunk-7-2.png)<!-- -->

| Female | Male | Girls |  Boys |
|-------:|-----:|------:|------:|
|    3.2 |  5.4 |  6.55 | 13.13 |

Average population with ADHD

| Women  | Men    |
|:-------|:-------|
| \~ 49% | \~ 43% |

Percentage of adults who still have ADHD

As I said previously, it is estimated that 15 to 65 % of children will
still have ADHD while growing up.  
On the last table, we can see that we still have an average of 49% of
6.55 % of girls who still have ADHD while growing up. For the men we
have a bit less than this average, since around 43% of the 13.13% of
boys with ADHD will still have the disorder as an adult. I also realized
a t.test which showed no significance for this difference of percentage
between male and female (p-value = 0.4473). Both 43% and 49% are in the
expected results of children who would keep the disorder in adulthood.

## Results

- **If we recap:**

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
      table](https://www.nimh.nih.gov/health/statistics/attention-deficit-hyperactivity-disorder-adhd#part_2553).
- Child and Adolescent Health Measurement Initiative. 2020-2021 National
  Survey of Children’s Health (NSCH) data query. Data Resource Center
  for Child and Adolescent Health supported by the U.S. Department of
  Health and Human Services, Health Resources and Services
  Administration (HRSA), Maternal and Child Health Bureau (MCHB).
  Retrieved from <https://mchb.hrsa.gov/data/national-surveys>
  - [Data
    table](https://www.childhealthdata.org/browse/survey/allstates?q=9343&g=1008&a=18062#)

### Pictures:

- \[@ADHD_couple\].(2020, October 4).Retrieved on
  [Instagram](https://www.instagram.com/p/CF7aB2NDL3j/?hl=f)
