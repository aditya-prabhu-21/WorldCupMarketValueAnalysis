### Predicting Professional Soccer Player Market Value Using FIFA World Cup Performance Statistics

**By Aditya Prabhu**

#### Executive summary
This project analyzed how player World Cup performance can predict the market value of professional soccer players. Separate models were created for defenders, midfielders, and forwards since each position uses different metrics to judge excellence. 

The results showed that World Cup statistics provide moderate predictive information about player market value. Mean absolute error was used as the scoring metric when choosing the models. Multiple Linear Regression was used for defenders and forwards while Ridge regression was used for midfielders. The models were then tasked to compare their predictions to the players' actual market value, in order to identify players who are underpriced, fairly priced, and overpriced based on their World Cup performance. 

#### Rationale
Professional soccer clubs invest millions of dollars in player transfers, so accurately assessing player value is critical to building competitive teams while managing budgets effectively. This analysis can help clubs identify players who are priced appropriately, avoid overpaying for players whose market value exceeds their performance, and find players whose contributions are not fully reflected in their transfer value. The results can support more informed player acquisitions, reducing financial risk and improving team performance. Without a data-driven approach, clubs may rely too heavily on subjective evaluations and reputation, leading to inefficient transfer decisions.

#### Research Question
To what extent can FIFA World Cup performance statistics predict the market value of professional soccer players, and do these statistics suggest that players are undervalued, fairly valued, or overvalued in the transfer market?

#### Data Sources
https://www.kaggle.com/datasets/mominullptr/fifa-world-cup-2026-dataset/data?select=squads_and_players.csv
https://www.kaggle.com/datasets/mominullptr/fifa-world-cup-2026-dataset/data?select=squads_and_players.csv

#### Methodology
Multiple regression techniques were used to determine which models best predict player market value. 
Multi Linear Regression was used as a baseline.
Ridge Regression was used to limit the bias of any one player statistic. 
Random Forest and Gradient Boosting were used to see if there were any non-linear relationships in the data.
Classification was used to predict whether a player is overvalued, undervalued, or fairly valued. 
Data visualization techniques such as scatter plots, heatmaps, and correlation analysis to explore relationships between player performance and market value.
Player stats to be analyzed will be determined by their position (e.g. defense, midfield, offense, goalie), meaning different features will drive a player's expected value

#### Results
The analysis found that World Cup performance statistics provide useful but incomplete information for predicting player market value. 

The strongest overall models were multiple linear regression for defenders/forwards and ridge regression for midfielders. Defender and midfielder models showed stronger predictive performance than the forward models. There were not that many non-linear relationships between player features, making both Random Forest and Gradient Boosting regressors unnecessary. Mean Absolute Error was used as the primary scoring mechanism for all these models because it tells us on average how far off the models predictive value is from the actual value. 

The majority of players in each position were classified as fairly priced, indicating that the selected models did a good job predicting valuations that reflect current market prices. The model also identified a meaningful number of potentially underpriced and overpriced players, revealing how the model was able to pinpoint oddities with current market valuations. 

Even though the World Cup hosted twice as many teams this year than any other world cup, the sample size for each position was relatively low compared to other data science studies. Thus, the model results should not be interpreted as a definitive assessment of what a player is worth, but as a screening tool used for scouting potential. 

That being said, the top three undervalued and overvalued players the models produced made a lot of sense. Amongst the top three undervalued players were Sadio Mane, Mikel Oyarzabal, and Deniz Undav. All three of these players had exceptional world cups and performed well over their current market value. The top three overvalued players were Mathias Olivera, Denis Zakaria, and Nicolas Seiwald. All three of these players came up short this world cup and did not perform to the level they were/are capable of. 


#### Next steps
This project was a good baseline to decide on whether a player is overvalued, undervalued, or fairly valued. Since this analysis was solely based on world cup statistics, it makes sense that the data provided to the models was limited. To make the model produce better predictive valuations, the project should incorporate data from club and past season/World Cup stats would. This would allow more factors to train on such as injury history, league strength, historical performances, individual accolades, etc. With the addition of more and more player features, we would be able to trim the error down significantly, making this project less of a screening tool and more of an actual predictor on player valuation. 

Another project that would be helpful for this project would be to create public data scrapers that log player stats after matches conclude. It was very hard to find football data that accurately represented player information, spanned over multiple seasons, and stayed updated. 

#### Project Link

- [Link to notebook 1](https://github.com/aditya-prabhu-21/WorldCupMarketValueAnalysis/blob/main/WorldCupAnalysis.ipynb)


##### Contact and Further Information
Aditya Prabhu
adityaprabhu21@gmail.com

