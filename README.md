# MPAA Ratings and Profitability - Exploratory Data Analysis

## Introduction

I have noticed over the years that many of the biggest blockbusters have been movies we could all enjoy going to see together as a family. Yet recently, it seems that there are fewer movies I feel I can comfortably take my younger children to.

This made me curious to explore what the drivers or motivations are for creating rated "R" movies vs lower rated movies.

This exploratory data analysis (EDA) investigates how movie content ratings (G, PG, PG-13, R) relate to earnings and profits.

The core questions are simple and practical:
* Which ratings are produced most often?
* Which MPAA ratings tend to earn more revenue?
* Which cost more to make?
* Which deliver higher profitability?
* Do “family-friendly” films (G/PG, or even PG-13) outperform R-rated films?
* How are these trends changing over time?

### Dataset Selection

The hardest thing to find was a good movies dataset that also included MPAA rating data. I ultimately combined two widely used movie datasets found on Kaggle.com:
* [Top Movies Ultimate Dataset](https://www.kaggle.com/datasets/michaelmatta0/movies-ultimate-metrics-features-and-metadata?select=Top+Movies+%28Raw+Data%29.csv )
* [Movies Dataset](https://www.kaggle.com/datasets/ashishkumarjayswal/movies-updated-data)

Both included title, year, MPAA rating, genre, production budget and worldwide gross. 

### Inspecting the Data

The first dataset contained a set of 5744 movies, with little missing data, however I wanted to make sure that it represented trends over the past 40 years, so I wanted to check and be sure the range of years it covered.

To supplement my data, I found another dataset of similar size and quality, but that appeared to have more movies from the 80s and 90s to round out my dataset.

My 2nd dataset looked great, but had over 1200 values equal to zero in the budget column. My datasets overlapped a little bit, so I was hoping that in merging the two, I could fill in some of the missing data.

### Merging the dataframes
I performed a full outer merge of `df` and `df2` based on 'title' and 'year'. This included all rows from both dataframes, creating a combined dataframe.

### Cleaning my merged dataframe

To clean my merged dataframe, I:
- looked at each column and checked for null values and zero values
- checked data types
- standardized field values
- tried to populate missing values or values == 0
- dropped data that I didn't need.
- created several new columns to make it easier to analyze my data.

#### Descriptive Statistics By MPAA Rating
With a solid dataset in place, I wanted to explore the different relationships between cost, revenue, profit, and ROI -- and see how they differ by MPAA rating.

#### Counts
First I wanted to get an idea of how many of each type of movie (by MPAA rating) there was to answer the question "Which ratings are produced most often?".

I believe this dataset is a good representation of most of the movies made in the past several decades. So although it may not include every movie made, it should include the vast majority of English speaking titles.









key insights

visualizations