---
title: "Statistical methods for archaeological data analysis I: Basic methods"
subtitle: "01 - Introduction"
author: "Martin Hinz"
institute: "Institut für Archäologische Wissenschaften, Universität Bern"
fontsize: 9pt
date: "20.02.2019"
output:
  xaringan::moon_reader:
    chakra: ../libs/remark-latest.min.js
    css: ["default", "default-fonts", "../libs/customize.css"]
    lib_dir: "libs"
    seal: false
    nature:
      beforeInit: "../libs/macros.js"
      highlightStyle: github
      highlightLines: true
      countIncrementalSlides: false
      fig_caption: yes
      ratio: "16:10"
---
class: title-slide, center, middle


# 

## 

### 

#### 



---

## Synopsis

.pull-left[
![](../images/01_session/snape.png)
]

.pull-right[
> "There will be no foolish wand-waving or silly incantations in this class. As such, I don't expect many of you to appreciate the subtle science and exact art that is statistics."
]
---

## Why statistics at all...

### For you:
Statistics are used! If you want to understand them, you have to learn it!

### For archaeology/science as discipline
Statistics make everything easier!

- Statements become more understandable and especially replicable
-Statistical statements are right or wrong no matter what reputation the scientist has
- Statements and data become comparable
- Getting the Knowledge of all the material for inductive understanding of scientific/archaeological relations takes decades, learning statistics only months

---

## Figures don't lie, but liars figure.
Samuel Clemens (alias Mark Twain)

### Statistics are only correct if question, approach and method are correct

e.g.: is social stratification observable on metal grave goods? Or on
jewellery? What if this depends on the (not observed) sex of the
deceased...

### Measuring and especially coding of measurements requires subjective decisions all the time:

Reasons for the decisions are often not understandable → subjective influence

### Statistics for statistics sake?
A logic (archaeologic) meaning have to be behind an analysis. And the results of analyses have to be logical (archaeological) testable.

---

## Statistic tool R: history (after Theus)

R is the successor of S resp. S-Plus

- S history:
  - 1976-1980: S-Version 1; (development by AT&T Labs) collection of Fortran routines
  - 1980-1984: S-Version 2 Porting to UNIX, definition of the command language
  - 1988-1991: S-Version 3 Porting to C, object-oriented, models
  - 1999-today:

S-Version 4 improved object-orientation (parallel the commercial version S-Plus)

- R history
  - early 90th: Development in New Zealand (R. Ihaka, R. Gentleman) Lisp based, only platform was Mac
  - middle 90th: expansion onto other platforms
  - end 90th: distributed development by the R-Core-Team

- R-Core-Team: 17 developers all over the world
- R-”specialists”: ca. 50 contributer
- developers of R-packages: hundreds, daily more

---

## Why R?

### Open Source

- Free accessible source code: transparency of the program
- Free to distribute: you don't have to pay horrific prices or make illegal copies

### Reference of the used algorithms

- Scientific citable

### Power

- The tool can do everything! Really! Exept making coffee...

### Spread

- Runs on all (major) operating systems
- Is widely used in the scientific field

---

## Why R?

### Disadvantages

- Command line: unfamiliar (new/old way to work with a computer)
- GUIs look different
- Knowledge of the english language is helpful
- Names of functions and parameters have to be kept in mind: is it col.names, colnames or header?
- Documentation is partly not very intuitiv: you should know what you are searching for

---

## Basic literature

### Stephan Shennan, Quantifying Archaeology.

The textbook for this course.

### David L. Carlson, Quantitative Methods in Archaeology Using R

A archaeology specific R textbook

### Dubravko Dolić, Statistik mit R.
### John Verzani, Using R for Introductory Statistics.

R-specific (introductory) statistical books

---

## More literature

- M. Fletcher/G. R. Lock, Digging Numbers: Elementary Statistics for Archaeologists. Oxford Univ. Comm. Arch. Monogr. 332 (Oxford 2005).
-  M. J. Baxter, Exploratory Multivariate Analysis in Archaeology (Edinburgh 1994).
-  M. Baxter, Statistics in Archaeology (London 2003).
-  P. Ihm, Statistik in der Archäologie: Probleme der Anwendung, allgemeine Methoden, Seriation und Klassifikation. Archaeo-Physika 9 (Köln 1978).
- J. Bortz, Statistik für Sozialwissenschaftler4 (Berlin u. a. 1993).

---

## Schedule

<table class="table table-striped table-hover" style="margin-left: auto; margin-right: auto;">
 <thead>
  <tr>
   <th style="text-align:left;"> date </th>
   <th style="text-align:left;"> topic </th>
   <th style="text-align:left;"> chapt. Shennan </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td style="text-align:left;"> 20.02.2019 </td>
   <td style="text-align:left;"> Introduction </td>
   <td style="text-align:left;"> 1+2 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> 27.02.2019 </td>
   <td style="text-align:left;"> Introduction into R </td>
   <td style="text-align:left;">  </td>
  </tr>
  <tr>
   <td style="text-align:left;"> 06.03.2019 </td>
   <td style="text-align:left;"> Explorative statistics - plots </td>
   <td style="text-align:left;"> 3 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> 20.03.2019 </td>
   <td style="text-align:left;"> Descriptive statistics </td>
   <td style="text-align:left;"> 4 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> 27.03.2019 </td>
   <td style="text-align:left;"> Nonparametric Tests </td>
   <td style="text-align:left;"> 5 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> 03.04.2019 </td>
   <td style="text-align:left;"> Chi-square test </td>
   <td style="text-align:left;"> 7 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> 10.04.2019 </td>
   <td style="text-align:left;"> Probability Theory </td>
   <td style="text-align:left;"> 5, 6, 14 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> 17.04.2019 </td>
   <td style="text-align:left;"> Distributions </td>
   <td style="text-align:left;"> 6 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> 01.05.2019 </td>
   <td style="text-align:left;"> Parametric Tests </td>
   <td style="text-align:left;"> 6 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> 08.05.2019 </td>
   <td style="text-align:left;"> Regression &amp; Correlation </td>
   <td style="text-align:left;"> 8 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> 15.05.2019 </td>
   <td style="text-align:left;"> Cluster Analysis </td>
   <td style="text-align:left;"> 11 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> 22.05.2019 </td>
   <td style="text-align:left;"> Correspondence Analysis </td>
   <td style="text-align:left;"> 13 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> 29.05.2019 </td>
   <td style="text-align:left;"> Test </td>
   <td style="text-align:left;">  </td>
  </tr>
</tbody>
</table>

---

## Flavours of statistics

- Descriptive statistics
  - Summary and description of data by using parameters (mean, standard deviation etc.)
- (graphical display)
  - Summary and description of data by using graphs (bar charts, pie charts etc.)
  - Useful for pattern detection and description, therefore intermediate position
- Explorative statistics
  - Summary and description of data for pattern detection (e.g. correspondence analysis)
- Statistical inference or statistical induction
  - testing of hypothesis on data (e.g. chi-squared test)

---

## Data, variables, values

- Variable:
  - What ist measured or analysed.
  - e.g. height
- item:
  - That whichs variable is measure
  - e.g. me as „possessor“ of a height, graves, persons...
- values:
  - The actual measurement.
  - e.g. my height is 1.81 m.
- discrete variable:
  - Variable which can take only certain values without intermediate values
  - e.g. income, counts of ceramic objects, sex (?)
- continuous Variablen:
  - Variable which can take all value and intermediate value
  - e.g. height, temperature, proportion value

---

## Flavours of Statistics 2

- univariate statistics:
  - Only on variable is involved
  - e.g. weight of bronze axes
- bivariate statistics:
  - Two variables are involved, of interest is their relation
  - e.g. relationship of length and width of bronze axes
- multivariate statistik:
  - More than two variables are involved, of interest is their relation
  - e.g. place of finding of axes (grave, depot, settlement) in relation to their chemical composition (proportion of copper, tin, arsenic, lead etc.)

---

## Independent – dependent variable

- Independent Variable:
  - The assumed cause of a relationship
- Dependent variable:
  - The assumed effect of the independent variable in a relationship
- example:
  - Number of pearls in a grave (Dependent) vs.
  - sex of the deceased (independent)
  - Hypothesis: The number of pearls in a grave depends on the sex of the deceased
- Can (have to be) not always to be defined
  - e.g.: volume and height of a vessel...

---

## Sample and Population

- Population:
  - Amount of all items of relevance for an analysis.
- sample
  - Selection of items on basis of certain criteria (e.g. representativity) which
  - will be analysed instead of the population
- Example opinion poll
  - Population: all federal citizens who have a meaning
  - Sample: the citizens who are polled by the polling organization

*complete enumeration of all the values ↔ sampling*

**In archaeology only sampling is possible! The population can never be investigated!**

---

## Levels of measurement

- nominal:
  - Categories which do not have a defined relationship among each other, only counting is possible (e.g. sex)
- ordinal:
  - Categories which are comparable and differ from each other in their characteristic [size/power/intensity]; their rank is determinable (e.g.
  - preservation conditions – bad, medium, good)
- metric:
  - Variable has a defined system of measurement, all calculations are possible. To distinguish are

1. interval: The variable has an arbitrary choosen neutral point (°C)
2. ratio: The variable has an absolute neutral point (°K)

- Sometimes also used: absolut scale
  - counts (number of inhabitans)

---

## Levels of Measurement

![](../images/01_session/scales_of_measurements.png)

---

## Levels of measurement

<table class="table table-striped table-hover" style="margin-left: auto; margin-right: auto;">
 <thead>
  <tr>
   <th style="text-align:left;"> scale </th>
   <th style="text-align:left;"> Meaningful statements </th>
   <th style="text-align:left;"> Examples </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td style="text-align:left;"> nominal </td>
   <td style="text-align:left;"> equality, inequality </td>
   <td style="text-align:left;"> Telephon numbers, illnesses, ceramic types </td>
  </tr>
  <tr>
   <td style="text-align:left;"> ordinal </td>
   <td style="text-align:left;"> bigger-smaller-relationship </td>
   <td style="text-align:left;"> Wind forces, academic ranks, classes of wealth, stratigraphic relations </td>
  </tr>
  <tr>
   <td style="text-align:left;"> interval </td>
   <td style="text-align:left;"> Equality of differences </td>
   <td style="text-align:left;"> Temperature in °C, calender age </td>
  </tr>
  <tr>
   <td style="text-align:left;"> ratio </td>
   <td style="text-align:left;"> Equality of ratios </td>
   <td style="text-align:left;"> Measurement of lengths, weight, height of a vessel </td>
  </tr>
</tbody>
</table>

.caption[after Bortz 2005]

---

## Levels of measurement

<table class="table table-striped table-hover" style="margin-left: auto; margin-right: auto;">
 <thead>
  <tr>
   <th style="text-align:left;"> scale </th>
   <th style="text-align:left;"> count </th>
   <th style="text-align:left;"> sort </th>
   <th style="text-align:left;"> difference </th>
   <th style="text-align:left;"> quotient </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td style="text-align:left;"> nominal </td>
   <td style="text-align:left;"> yes </td>
   <td style="text-align:left;"> no </td>
   <td style="text-align:left;"> no </td>
   <td style="text-align:left;"> no </td>
  </tr>
  <tr>
   <td style="text-align:left;"> ordinal </td>
   <td style="text-align:left;"> yes </td>
   <td style="text-align:left;"> yes </td>
   <td style="text-align:left;"> no </td>
   <td style="text-align:left;"> no </td>
  </tr>
  <tr>
   <td style="text-align:left;"> interval </td>
   <td style="text-align:left;"> yes </td>
   <td style="text-align:left;"> yes </td>
   <td style="text-align:left;"> yes </td>
   <td style="text-align:left;"> no </td>
  </tr>
  <tr>
   <td style="text-align:left;"> ratio </td>
   <td style="text-align:left;"> yes </td>
   <td style="text-align:left;"> yes </td>
   <td style="text-align:left;"> yes </td>
   <td style="text-align:left;"> yes </td>
  </tr>
</tbody>
</table>

.caption[after Bortz 2005]

---

## Levels of measurement

Change of the level

- downscaling:
  - Always possible.
  - e.g. classification of measurements (small-medium-big)
  - But: leads to loss of information
- upscaling:
  - Sometimes possible
  - e.g.: instead of classification of ceramics in coarse-fine ware measurement of grain size
  - But: leads to larger data volume and higher complexity of measurement
- Conclusion:
  - For analysis should the best fitting level of measurement be choosen.
  - Because there can always occure a change in the requirements, rule of thumb: take one level finer than you think you will need in the end (as said, just a rule of thumb...)

---

## Data collection: list

Simple list of the data

example:

```
##  [1] 154 167 187 165 190 176 167 156 154 165 167 171 154
```

---

## data preparation: matrix of data
Table of multiple values each item

example:
.tiny[
<table class="table table-striped table-hover" style="margin-left: auto; margin-right: auto;">
 <thead>
  <tr>
   <th style="text-align:left;"> name </th>
   <th style="text-align:left;"> height </th>
   <th style="text-align:left;"> sex </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td style="text-align:left;"> Hannah </td>
   <td style="text-align:left;"> 154 </td>
   <td style="text-align:left;"> 2(female) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Leon </td>
   <td style="text-align:left;"> 167 </td>
   <td style="text-align:left;"> 1(male) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Lukas </td>
   <td style="text-align:left;"> 187 </td>
   <td style="text-align:left;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Leonie </td>
   <td style="text-align:left;"> 165 </td>
   <td style="text-align:left;"> 2 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Luka </td>
   <td style="text-align:left;"> 190 </td>
   <td style="text-align:left;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Lea </td>
   <td style="text-align:left;"> 176 </td>
   <td style="text-align:left;"> 2 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Lena </td>
   <td style="text-align:left;"> 167 </td>
   <td style="text-align:left;"> 2 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Mia </td>
   <td style="text-align:left;"> 156 </td>
   <td style="text-align:left;"> 2 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Tim </td>
   <td style="text-align:left;"> 154 </td>
   <td style="text-align:left;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Fynn </td>
   <td style="text-align:left;"> 165 </td>
   <td style="text-align:left;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Anna </td>
   <td style="text-align:left;"> 167 </td>
   <td style="text-align:left;"> 2 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Emily </td>
   <td style="text-align:left;"> 171 </td>
   <td style="text-align:left;"> 2 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Felix </td>
   <td style="text-align:left;"> 154 </td>
   <td style="text-align:left;"> 1 </td>
  </tr>
</tbody>
</table>
]
---

## data preparation: “tally sheet” / frequency table

Table of multiple items each value
example:

<table class="table table-striped table-hover" style="margin-left: auto; margin-right: auto;">
 <thead>
  <tr>
   <th style="text-align:left;"> name </th>
   <th style="text-align:left;"> Tally marks </th>
   <th style="text-align:left;"> counts </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td style="text-align:left;"> 154 </td>
   <td style="text-align:left;"> ||| </td>
   <td style="text-align:left;"> 3 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> 156 </td>
   <td style="text-align:left;"> | </td>
   <td style="text-align:left;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> 167 </td>
   <td style="text-align:left;"> ||| </td>
   <td style="text-align:left;"> 3 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> 165 </td>
   <td style="text-align:left;"> || </td>
   <td style="text-align:left;"> 2 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> 171 </td>
   <td style="text-align:left;"> | </td>
   <td style="text-align:left;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> 176 </td>
   <td style="text-align:left;"> | </td>
   <td style="text-align:left;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> 187 </td>
   <td style="text-align:left;"> | </td>
   <td style="text-align:left;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> 190 </td>
   <td style="text-align:left;"> | </td>
   <td style="text-align:left;"> 1 </td>
  </tr>
</tbody>
</table>

---

## data preparation: classification

Table of multiple items each class of value

example:

<table class="table table-striped table-hover" style="margin-left: auto; margin-right: auto;">
 <thead>
  <tr>
   <th style="text-align:left;"> name </th>
   <th style="text-align:left;"> Tally marks </th>
   <th style="text-align:left;"> counts </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td style="text-align:left;"> &lt;150 </td>
   <td style="text-align:left;">  </td>
   <td style="text-align:left;"> 0 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> 150-159 </td>
   <td style="text-align:left;"> |||| </td>
   <td style="text-align:left;"> 4 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> 160-169 </td>
   <td style="text-align:left;"> ||||| </td>
   <td style="text-align:left;"> 5 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> 170-179 </td>
   <td style="text-align:left;"> || </td>
   <td style="text-align:left;"> 2 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> 180-189 </td>
   <td style="text-align:left;"> | </td>
   <td style="text-align:left;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> &gt;190 </td>
   <td style="text-align:left;"> | </td>
   <td style="text-align:left;"> 1 </td>
  </tr>
</tbody>
</table>

Class width here 10 cm

Rule of thumb: ca. 8 – 12 classes or

Number of classes $k ≈ \sqrt{n}$, here therefore $k ≈ \sqrt{13} = 3.6055513 ≈ 4$

---

## Equations & symbols

|||
|-|-|
| ca. | $a≈b$ |
| count | $n$ |
| sum | $\sum_{i=1}^n x_i$ |
| This means | $x_1 =0, x_2 =4, x_3 =5, x_4 =2, x_5 =1, x_6 =1 ; n=6$
|  | $x_1 + x_2 + x_3 + x_4 + x_5 + x_6 =\sum_{i=1}^n x_i$ |
| Product the same way | $\prod_{i=1}^n x_i = x_1 ∗x_2 ∗x_3 ∗x_4 ∗x_5 ∗x_6 = 0$ |

---

## Example arithm. mean

$$ \bar{x}=\frac{\sum_{i=1}^n x_i} n $$

observations : x i :={154,167,187,165,190,176, 167,156,154,165,167,171, 154}

number of observations : n=13

$$ \bar{x}=\frac{154 + 167 + 187 + 165 + 190 + 176 + 167 + 156 + 154 + 165 + 167 + 171 + 154} {13} \\\\
\bar{x}=\frac{2173} {13} \\\\
\bar{x}=167.1538462 $$

---

## exercise: description of the participants

**Make 5 groups and carry out a data collection about the participants**

Data to collect for the groups

- A) Email, number of the computer in front of you
- B) Sex, Age
- C) laptop yes/no, foot size
- D) actual cash in your purse, height
- E) homecountry, operation system used at home

Collect the data matrix (use a spreadsheet software of your choice), determine the level of measurement of each variable and present your results in 10 min.

---

## exercise: description of the participants

### Conclusion:
Data collection needs a systematic. This will be best developed with a small sample ('pilot study'). After this the whole planned data collection should be carried out according to the developed scheme equal for all items.

Information can be of very varying kind (level of measurement)

For all kinds of information there are different ways of presenting them...
