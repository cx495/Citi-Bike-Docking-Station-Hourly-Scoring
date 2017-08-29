# CITIBIKE DOCKING STATION SCORING

Citi Bike has a Bike Angel program where they incentivize people to rebalance their bikes. <br>They use scores to encourage users to rebalance the bikes so they could reduce the cost on rebalancing bikes using trucks.<br> Currently there is a set of scores for the morning then another for the evening commute. <br>I developed a new methodology for scoring each of the stations, a more dynamic scoring function as an hourly scoring.


http://www.slate.com/blogs/moneybox/2017/02/09/new_york_s_citi_bike_pays_riders_to_make_it_run_better.html

http://bikeangels.citibikenyc.com/


## Scoring Function:
## score (dh, df, w)

## Function Input:
dh - Date Hour to score such as '2017030821' - "2017030905"

df - Data Frame of Prescores of past 3 hours before Date Hour (It usually requires Citi Bike Histories data from the past 3 days to make the Data Frame of Prescores of past 3 hours)

 w - Scoring Standard such as w = [0.05, 0.1, 0.1, 0.5, 0.1, 0.1, 0.05], which means after sorting the stations by their prescores from min to max, successively give %5 of stations the score of -3, %10 of stations the score of -2, 10% of stations the score of -1, 50% of stations the score of 0, 10% of stations the score of 1, 10% of stations the score of 2, 5% of stations the score of 3.

## Function Output:
Scoring Table - Scores of each station at the Date Hour 
