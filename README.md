# Linear Regression - Tennis
## Project Goals
Create a linear regression model that predicts the outcome for a tennis player based on their playing habits.

## built with
* Python 3
* Jupyter Notebook

## data sources
Men's Professional Tennis League; Association of Tennis Professionals (downloaded from Codecademy)

### Identifying Data
Field | Description
------------ | -------------
Player | name of the tennis player
Year | year data was recorded

### Service Game Columns (Offensive)
Field | Description
------------ | -------------
Aces | number of serves by the player where the receiver does not touch the ball
DoubleFaults | number of times player missed both first and second serve attempts
FirstServe | % of first-serve attempts made
FirstServePointsWon | % of first-serve attempt points won by the player
SecondServePointsWon | % of second-serve attempt points won by the player
BreakPointsFaced | number of times where the receiver could have won service game of the player
BreakPointsSaved | % of the time the player was able to stop the receiver from winning service game when they had the chance
ServiceGamesPlayed | total number of games where the player served
ServiceGamesWon | total number of games where the player served and won
TotalServicePointsWon | % of points in games where the player served that they won

### Return Game Columns (Defensive)
Field | Description
------------ | -------------
FirstServeReturnPointsWon | % of opponents first-serve points the player was able to win
SecondServeReturnPointsWon | % of opponents second-serve points the player was able to win
BreakPointsOpportunities | number of times where the player could have won the service game of the opponent
BreakPointsConverted | % of the time the player was able to win their opponent’s service game when they had the chance
ReturnGamesPlayed | total number of games where the player’s opponent served
ReturnGamesWon | total number of games where the player’s opponent served and the player won
ReturnPointsWon | total number of points where the player’s opponent served and the player won
TotalPointsWon | % of points won by the player

### Outcomes
Field | Description
------------ | -------------
Wins| number of matches won in a year
Losses| number of matches lost in a year
Winnings| total winnings in USD($) in a year
Ranking| ranking at the end of year

## acknowledgements
* Association of Tennis Professionals, downloaded from Codecademy
* [Codecademy Data Scientist Skill Path](https://www.codecademy.com/learn)
