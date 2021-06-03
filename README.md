### Betting on 21.5
##### **MID-TERM project | A simple strategy to beat the bookies using ML.**

### The dataset
The tennis dataset `shape` is (28335,42). It can be found here: [tennis-data.co.uk](http://tennis-data.co.uk/alldata.php).
<br />
<br />

### Columns Description:

- |__ATP__| -> Tournament ID. _'int64'_
- |__Location__| -> Location of the tournament. _'object'_
- |__Tournament__| -> Name of the Tournament _'object'_
- |__Date__| -> Date of the tournament. _'datetime'_
- |__Series__| -> Type of tournament. _'object'_
- |__Court__| -> Surface of the match. _'object'_
- |__Round__| -> Round of the competition. _'object'_
- |__Best of__| -> Max amount of sets that can be played in a match. _'float64'_
- |__Winner__| & |__Loser__| -> Winner/Loser of the match. _'object'_
- |__LRank__| & |__Loser__| -> ATP Rank of the winner/loser. _'float64'_
- |__WPts__| & |__LPts__| -> ATP points in Rank of the winner/loser. _'float64'_
- |__W1__| - |__W5__|, |__L1__| - |__L5__| -> Games won or lost by each player on that match. _'float64'_
- |__Comment__| -> Comments on the state of the match. _'object'_  
- |__Wsets__| & |__Lsets__| -> Sets won by the winner/loser. _'float64'_
- |__B365W__| & |__B365W__| -> Bookies odds (Bet 365). _'float64'_
- |__EXW__| & |__EXL__| -> Bookies odds (Express). '_float64'_ _'object'_
- |__SJW__| & |__SJL__| -> Bookies odds (SJ). _'float64'_
- |__PSW__| & |__PSL__| -> Bookies odds (Pinnacle). _'float64'_
- |__LBW__| & |__LBL__| -> Bookies odds (Liberty). _'float64'_
- |__MaxW__| & |__MaxL__| -> Max odds offered taken oddsport. _'float64'_
- |__MinW__| & |__MinL__| -> Mix odds offered taken oddsport. ??
- |__AvgW__| & |__AvgL__| -> Avg odds offered. _'float64'_



### Introduction
For the midterm project at Ironhack we decided to find a way to get rich quickly (jokes on us :smile:). We focused on a simple analysis of the betting market and tried to build a strategy to beat the bookies using Machine Learning. We picked every [major tournament](https://en.wikipedia.org/wiki/2020_ATP_Challenger_Tour) ie; ATPs, GrandSlams, Masters and MasterCups played from 2010-2021 and skipped 'small' tournaments like [Challengers](https://en.wikipedia.org/wiki/2020_ATP_Challenger_Tour) or [ITFs](https://en.wikipedia.org/wiki/International_Tennis_Federation).Compared to other sports like football where that number of matches is reached by the first and second division of any single European country we needed to squeeze the volumen in order to reduce the variance.

We only took into account ATP [ranked](https://www.atptour.com/en/rankings/singles) players.
<br />
<br />

### Goal
- Get a positive Return on Investment **(ROI)**.
- Big volume of matches.
- Find our niche (OVER/UNDER 21.5).
<br />
<br />

### Rules of tennis
Check [here](https://www.rulesofsport.com/sports/tennis.html) the rules of tennis.
<br />
<br />

### How does tennis betting work in a nutshell?
Let's say you bet 10€ on Nadal with an odd of 1.5: 
1. If he wins, you go back home with your 10€, plus 5€ of benefits.
2. If he loses you go back home with 0€
3. If he wins, as you bet 10€ and won 15€, your ROI (return on investment) is 50% on that specific bet.
4. If he looses, your ROI in -100%

If you want to dig deeper on how tennis betting work: Click [here](https://www.rookieroad.com/tennis/how-does-tennis-betting-work/).

For our specific market target (**OVER/UNDER 21.5**). Click [here](https://www.rookieroad.com/tennis/what-215-mean-tennis-betting/).
<br />
<br />

### Understanding the impact of ROI,YEILD & BEP.
*ROI or Return on Investment is a measure of the efficiency of an investment – or how much money you can expect to make relative to the amount of money you risk.*

> PROFIT = (Wager Return - Amount Wagered)

> **ROI**= PROFIT / AMOUNT_WAGERED

The ROI in the above example would be equal to **5€** or **50%** if our pick wins.
<br />
<br />

*Yield is a percentage calculation of the betting efficiency, depending on the selected bets and odds for the match or bet slip.*

> #= Number of bets 

> **YEILD** = (Profit - #) / #

Yield and ROI have a very similar formula. The difference is that ROI gives you your profit/loss ratio related to your initial investment, while yield gives you your average win on the turnover, for each of your individual bets.
<br />
<br />

*The BEP or Break Even Point is that magical number where if we win this percentage of the time we’ll at the very least not lose money, and ideally go beyond that to make a nice return on their investment.*

> **BEP** = 1 / odds 

Using 1.80 odds (more or less the avg offered by the bookies for the over/under 21.5 in tennis), we'd need to win 55.55% of the time. If we rounded up, we could say that anything above 56% in the long run is net profit.*
<br />
<br />