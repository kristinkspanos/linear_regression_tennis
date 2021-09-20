# Linear Regression - Tennis
## project goals
Create linear regression models to predict outcomes for a tennis player based on their playing habits. This Codecademy project includes the following prompts:
* Perform exploratory analysis on the data by plotting different features against the different outcomes. What relationships do you find between the features and outcomes? Do any of the features seem to predict the outcomes?
* Use one feature from the dataset to build a single feature linear regression model on the data. Your model, at this point, should use only one feature and predict one of the outcome columns. Before training the model, split your data into training and test datasets so that you can evaluate your model on the test set. How does your model perform? Plot your model’s predictions on the test set against the actual outcome variable to visualize the performance.
* Create a few more linear regression models that use one feature to predict one of the outcomes. Which model that you create is the best?
* Create a few linear regression models that use two features to predict yearly earnings. Which set of two features results in the best model?
* Create a few linear regression models that use multiple features to predict yearly earnings. Which set of features results in the best model?

## results
* Single feature linear regression
  * Model A
    * x = ReturnPointsWon, y = ReturnGamesWon
    * R² for the training test: 0.76, R² for the testing test: 0.76
    * Interpretation: The R² for the test and training sets are similar, indicating that the model generalizes the data well. An R² value of 0.76 indicates that the model explains 76% of the variation in the model, which is a strong result.
  * Model B
    * x = ServiceGamesPlayed, y = Aces
    * R² for the training test: 0.76
    * R² for the testing test: 0.73
    * Interpretation: The R² for the test and training sets are similar, indicating that the model generalizes the data well. An R² value of 0.73 for the testing set indicates that the model explains 73% of the variation in the model, which is a strong result.
  * Model C
    * x = FirstServePointsWon, y = Wins
    * R² for the training test: 0.12
    * R² for the testing test: 0.14
    * Interpretation: The R² for the test and training sets are similar, indicating that the model generalizes the data well. An R² value of 0.14 for the testing set indicates that the model explains 14% of the variation in the model, which is a weak result.
* Two feature lienar regression
  * Model D
    * x = ReturnGamesPlayed, ServiceGamesPlayed, y = Winnings
    * R² for the training test: 0.84
    * R² for the testing test: 0.83
    * Interpretation: The R² for the test and training sets are similar, indicating that the model generalizes the data well. An R² value of 0.83 for the testing set indicates that the model explains 83% of the variation in the model, which is a weak result.
  * Model E
    * x = DoubleFaults, BreakPointsOpportunities, y = Winnings  
    * R² for the training test: 0.82
    * R² for the testing test: 0.83
    * Interpretation: The R² for the test and training sets are similar, indicating that the model generalizes the data well. An R² value of 0.83 for the testing set indicates that the model explains 83% of the variation in the model, which is a weak result.
* Multiple linear regression 
  * Model F
    * x = ServiceGamesPlayed, ReturnGamesPlayed, Wins, Losses, y = Winnings
    * R² for the training test: 0.87
    * R² for the testing test: 0.85
    * Interpretation: The R² for the test and training sets are similar, indicating that the model generalizes the data well. An R² value of 0.85 for the testing set indicates that the model explains 85% of the variation in the model, which is a weak result.
  * Model G
    * x = Aces, BreakPointsFaced, BreakPointsOpportunities, DoubleFaults, ReturnGamesPlayed, ServiceGamesPlayed, Wins, Losses, y = Winnings
    * R² for the training test: 0.87
    * R² for the testing test: 0.85
    * Interpretation: The R² for the test and training sets are similar, indicating that the model generalizes the data well. An R² value of 0.85 for the testing set indicates that the model explains 85% of the variation in the model, which is a weak result.

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
