# Bachelor Thesis: Analysis of the efficiency in betting markets: A replication study for the favorite-longshot-bias in the tennis betting market

Oddsmaker trying to publish odds, which reflect the outcome probabilities (adjusted with their vig) of the games. But the odds are not fixed, the oddsmaker adjusts them dependent on the betting volume. So, the oddsmaker wants to balance the volume out to have a sure win. Because of that odds are not every time efficient. The punters underlie some biases, which skew the real probability of the odds.
One of the most researched phenom in the betting markets is the favorite-longshot-bias (FLB). The favorite-longshot-bias means that favorites are undervalued by the odds and underdogs are overvalued. In the tennis market, the first who could show an FLB were Forrest and McHale (2007). On their work, I build my analysis. I backtested the games and odd from the last 18 men's tennis seasons (2002-2020). For that, I use a logistic regression model.

## Key findings

* From 2002 to 2012 and 2014 to 2015 there is a significant FLB. But since 2016 the trend shows, that the FLB has not a significant effect on the betting market.

![alt text](https://github.com/Schlon24/Efficiency-of-tennis-betting-market/blob/master/images/Comparison_Saisons.png)

* The FLB effect is stronger if you are betting favorites in a major tournament (expected return -0,009 %)

* Also higher FLB effect if both players are outside top 50 in the rankings  (expected return -0,01 %)

* Matches in a major tournament and with players outside the top 50 you would make some money (expected return 0,0169 %)

![alt text](https://github.com/Schlon24/Efficiency-of-tennis-betting-market/blob/master/images/return_matrix.png)

## Code and Resources Used 
* Python Version: 3.7  
* Packages: pandas, numpy, glob, sklearn, matplotlib, seaborn, sciPy, statsmodels, geopy
* Data: http://www.tennis-data.co.uk/alldata.php

## Part 1: Descriptive Analysis
Descriptive comparison between the data from the original study (Forest and McHale, 2007) and the new data:
* Odds interval
* Split the data into different seasons
* Only data from major tournaments (Grand Slams)

## Part 2: The Model
* Data preparation
  * Divide into favorites (fav) and Outsiders (out)
  * Random selection of a player to bet for every match
* Linear regression
* Logistic regression

## Part 3: The Analysis
Adding variables:
- GS = All matches in a grand slam tournament
- LowRank = Two players outside the top 50
- LowRound = First Round of the tournament

## Literature
- Forrest, D. & McHale, I. (2007). Anyone for tennis (betting)? The European Journal of
Finance, 13 (8), 751–768. doi: 10.1080/13518470701705736
- Koning, R. H. (2012). Regression tests and the efficiency of fixed odds betting markets.
International Journal of Sport Finance, 7 , 262–274.
- Lahvička, J. (2014). What causes the favourite-longshot bias? further evidence from
tennis. Applied Economics Letters, 21 (2), 90–92. doi: 10.1080/13504851.2013
.842628
- Woodland, L. & Woodland, B. (1999). Expected utility, skewness, and the baseball bet-
ting market. Applied Economics, 31 (3), 337–345. doi: 10.1080/000368499324327

