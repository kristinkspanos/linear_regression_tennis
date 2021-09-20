# Linear Regression - Tennis
## project goals
Create linear regression models to predict outcomes for a tennis player based on their playing habits. This Codecademy project includes the following prompts:
* Perform exploratory analysis on the data by plotting different features against the different outcomes. What relationships do you find between the features and outcomes? Do any of the features seem to predict the outcomes?
* Use one feature from the dataset to build a single feature linear regression model on the data. Your model, at this point, should use only one feature and predict one of the outcome columns. Before training the model, split your data into training and test datasets so that you can evaluate your model on the test set. How does your model perform? Plot your model’s predictions on the test set against the actual outcome variable to visualize the performance.
* Create a few more linear regression models that use one feature to predict one of the outcomes. Which model that you create is the best?
* Create a few linear regression models that use two features to predict yearly earnings. Which set of two features results in the best model?
* Create a few linear regression models that use multiple features to predict yearly earnings. Which set of features results in the best model?

## results
The dataset contains two types of numeric variables - proportional variables that are scaled to be shown as a percentage (i.e. ServiceGamesWon), and variables that show the total count of an event (i.e. ServiceGamesPlayed). The variables that represent the total count of an event are most likely to explain the variable 'Winnings', because 'Winnings' also represents a cumulative value. In the models below, proportional variables are shown with a (p), and cumulative variables are shown with a (c).

### single feature linear regression
* Model A
  * x = ReturnPointsWon (p), y = ReturnGamesWon (p)
  * R² for the training test: 0.76
  * R² for the testing test: 0.76
  * Interpretation: The R² for the test and training sets are similar, indicating that the model generalizes the data well. An R² value of 0.76 indicates that the model explains 76% of the variation in the model, which is a strong result.
* Model B
  * x = ServiceGamesPlayed (c), y = Aces (c)
  * R² for the training test: 0.76
  * R² for the testing test: 0.73
  * Interpretation: The R² for the test and training sets are similar, indicating that the model generalizes the data well. An R² value of 0.73 for the testing set indicates that the model explains 73% of the variation in the model, which is a strong result.
* Model C
  * x = FirstServePointsWon (p), y = Wins (c)
  * R² for the training test: 0.12
  * R² for the testing test: 0.14
  * Interpretation: The R² for the test and training sets are similar, indicating that the model generalizes the data well. An R² value of 0.14 for the testing set indicates that the model explains 14% of the variation in the model, which is a weak result. This weak results may result because FirstServePointsWon is a percentage, and Wins is a count.
### two feature lienar regression
* Model D
  * x = ReturnGamesPlayed (c), ServiceGamesPlayed (c), y = Winnings
  * R² for the training test: 0.84
  * R² for the testing test: 0.83
  * Interpretation: The R² for the test and training sets are similar, indicating that the model generalizes the data well. An R² value of 0.83 for the testing set indicates that the model explains 83% of the variation in the model, which is a weak result.
* Model E
  * x = DoubleFaults (c), BreakPointsOpportunities (c), y = Winnings  
  * R² for the training test: 0.82
  * R² for the testing test: 0.83
  * Interpretation: The R² for the test and training sets are similar, indicating that the model generalizes the data well. An R² value of 0.83 for the testing set indicates that the model explains 83% of the variation in the model, which is a weak result.
### multiple linear regression 
* Model F
  * x = ServiceGamesPlayed (c), ReturnGamesPlayed (c), Wins (c), Losses (c), y = Winnings
  * R² for the training test: 0.87
  * R² for the testing test: 0.85
  * Interpretation: The R² for the test and training sets are similar, indicating that the model generalizes the data well. An R² value of 0.85 for the testing set indicates that the model explains 85% of the variation in the model, which is a weak result.
* Model G
  * x = Aces (c), BreakPointsFaced (c), BreakPointsOpportunities (c), DoubleFaults (c), ReturnGamesPlayed (c), ServiceGamesPlayed (c), Wins (c), Losses (c), y = Winnings
  * R² for the training test: 0.87
  * R² for the testing test: 0.85
  * Interpretation: The R² for the test and training sets are similar, indicating that the model generalizes the data well. An R² value of 0.85 for the testing set indicates that the model explains 85% of the variation in the model, which is a weak result.

## ideas for additional analysis
Calculate a variable that shows the pct. of matches that a player won in a year ( 'Wins' / ('Wins' + 'Losses')). Create linear regression models using the proportional variables in the dataset to analyze which variables predict wins as a pct. of total matches played.

## built with
* Python 3
* Jupyter Notebook

## data sources
Association of Tennis Professionals (downloaded from Codecademy)

### Identifying Data
Field | Description
------------ | -------------
Player | name of the tennis player
Year | year data was recorded

### service game columns (offensive)
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

### return game columns (defensive)
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

### outcomes
Field | Description
------------ | -------------
Wins| number of matches won in a year
Losses| number of matches lost in a year
Winnings| total winnings in USD($) in a year
Ranking| ranking at the end of year

## acknowledgements
* Association of Tennis Professionals, downloaded from Codecademy
* [Codecademy Data Scientist Skill Path](https://www.codecademy.com/learn)
