Math 295: Homework 3
================
Be Sure to Put Your Name Here
Due February 9, 2021

  - [Introduction](#introduction)
  - [Movie Data Analysis](#movie-data-analysis)
      - [Data Overview](#data-overview)
      - [Exploratory Data Analysis](#exploratory-data-analysis)
      - [Wrangling the Movie Data](#wrangling-the-movie-data)

# Introduction

Use this document as a template for writing up your assignment. You
should delete this line before submitting. Remove the `eval=FALSE`
option on line 16 so that your chunks will be executed when you knit
this file. Also, remember that you can adjust the default figure height
and width dimensions in the YAML section at the top or at the code chunk
level.

# Movie Data Analysis

In this analysis, you will investigate IMDB and Rotten Tomatoes ratings
for a random sample of 651 movies. The following command loads the data
into a dataframe named `movies.`.\[1\]

``` r
# load the data from an R binary data file into the data frame movies 
load(file = "data/movies.Rdata")
```

## Data Overview

1.  Use the R command that will give an overview of the `movies` data
    frame by showing all the variable names and the first few
    observations from each.

**Answer:**

## Exploratory Data Analysis

2.  Use `count()` to obtain frequency tables for four factor variables:
    `title_type`, `genre` and `critics_rating` and `audience_rating`.

**Answer:**

3.  Make a histogram of **imdb\_rating**.

**Answer:**

4.  Repeat the previous histogram but this time pick a binwidth such
    that each bar will correspond to just one distinct value of the
    `imdb_rating` variable.

**Answer:**

5.  Write two or three sentences summarizing your observations about the
    `imdb_rating` scores.

**Answer:**

6.  Create a scatterplot comparing the Rotten Tomatoes `critic_score`
    (y) to imdb ratings (x).Add a smoothing line (no standard error
    band). If necessary, add jittering to avoid overplotting.

**Answer:**

7.  Now try some alternatives to traditional scatterplots for exploring
    the relationship between these two variables. In practice, some of
    these would be more appropriate for larger data sets but show that
    you can construct them for this pair of variables. Create each of
    the following plots described in the text of this section: (i)
    `geom_bin2d()`; (ii) `geom_hex()`; and (iii) a boxplot using either
    `cut_width()` or `cut_number()` that has ten boxes and whose width
    is proportional to the number of movies represented.

**Answer:**

8.  Inspect your scatterplots from part (f) and (g) and write a couple
    sentences observing the nature, strength and direction of the
    covariation of these two variables.

**Answer:**

8.  Use faceting to consider whether the relationship between Rotten
    Tomatoes rating and IMDB rating depends on the MPAA ratings. For
    each facet, add a least squares regression line without a standard
    error bar and write a couple sentences with your observations.

**Answer:**

1.  Instead of faceting, create a graph that shows how the relationship
    between IMDB rating and Rotten Tomatoes rating is related to
    `runtime`. That is, add `runtime` as a third variable to your
    scatterplot from (f) and map it to an aesthetic. You may find it
    useful to make use of one of the `cut_` functions for incorporating
    `runtime`. Comment on what you see.

**Answer:**

## Wrangling the Movie Data

10) Use `select()` to create a new data set **movies2** containing just
    the following variables: `title`, `runtime`, `genre`, `mpaa_rating`,
    `thtr_rel_year`, `imdb_rating`, `imdb_num_votes`, `critics_score`,
    `audience_score`, and `best_pic_win`.

**Answer:**

11) Compute the means of all the numeric variables. Note which variables
    have NA values for their means.

**Answer:**

12) You should have found that the `runtime` variable is missing for at
    least one movie. Identify the movie(s) missing `runtime` data and
    track down (Google) the missing data. Replace the NA value(s) with
    their correct value(s) and re-compute the mean for `runtime`.

**Answer:**

13) Compute the mean `runtime` for each `genre` and then create a bar
    chart of the mean `runtime` by `genre`. Which genres have the lowest
    and highest average `runtime`?

**Answer:**

1.  This problem adapts a tutorial prepared by Iain Carmichael and makes
    use of the movies data generously provided by Mine Cetinkaya-Rundel.
    The original data set is available at her
    [website](http://www2.stat.duke.edu/~mc301/data/movies.html).
