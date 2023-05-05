# PUBG-DATA-ANALYSIS-1
PUBG DATA ANALYSIS
PlayerUnknown’s Battlegrounds (PUBG) is a highly competitive game that has captured the attention of millions of players worldwide. With global tournaments offering cash prizes, the game has become a platform for serious players to showcase their skills and compete at the highest level. However, the odds of winning are slim, as each game begins with 100 players, and only one can emerge victorious. This has led to a huge demand for winning tactics and tips, with thousands of searches conducted daily. To address this need, we conducted a data analysis of PUBG gameplay to identify key actions that could improve a player’s chances of survival, increase their kills, and ultimately lead to a higher chance of winning. By gathering and analyzing relevant data, we aim to provide players with valuable insights that can help them improve their gameplay and achieve better results in PUBG.

* **Task 1:-Prepare a complete data analysis report on the given data.**

* **Task 2:-Create a predictive model which is an attempt to predict the win probability
of the Pubg match and to look at the important factors affecting the win probability of
the pubg game.**


**Feature Analysis**


* **groupId** - ID to identify a group within a match
* **matchId** - ID to identify match(Maximum 100 players in each max)
* **assists** - Number of enemy players this player damaged that were killed by teammates
* **boosts** - Number of boost items used(energy drinks)
* **damageDealt** - Total damage dealt.
* **DBNOs** - Number of enemy players knocked.
* **headshotKills** - Number of enemy players killed with headshots.
* **heals** - Number of healing items used(Painkillers,healthkit)
* **killPlace** - Ranking of a player in a match based on kills
* **killPoints** - Points based on kills
* **kills** - Number of enemy players killed.
* **killStreaks** - Max number of enemy players killed in a short amount of time.
* **longestKill** - Longest kill distance of player
* **maxPlace** - players or team position in a game(There will be difference based on type of the game)
* **numGroups** - Number of groups joined or playing in a match
* **revives** - Number of times this player revived teammates.
* **rideDistance** - Total distance traveled in vehicles measured in meters.
* **rank points** - Players current rank
* **roadKills** - Number of kills while in a vehicle.
* **swimDistance** - Total distance traveled by swimming measured in meters.
* **teamKills** - Number of times this player killed a teammate.
* **vehicleDestroys** - Number of vehicles destroyed.
* **walkDistance**- Total distance traveled on foot measured in meters.
* **weaponsAcquired** - Number of weapons picked up.
* **winPoints** - Points earned after the game(based on survival time,assists,kills,maxplac etc)
* **winPlacePerc** - The target of prediction. This is a percentile winning placement, where 1 corresponds to 1st place, and 0 corresponds to last place in the match.

**Performance of Top 3 Models**

* Model Creation using linear regression,GB regressor,and Decision tree regressor didnot come as expected(Gives an R2 which is less than 90 ).
* **XGB Regression** : XGB regressor gives good result with default parameters.We got an R2 of 91 and Adjusted R2 90,but after parameter tuning R2 score was reduced to 87..
* **Random Forest Regression** :  We expected that random forest would work better as the model would not be on an assumption that the winPlacePerc is a linear combination of the inputs. At the cost of more time taken for fit(2 hours), random forest is able to discover more complex dependencies.We got good R2(91.5) and less MSE(0.087) .But after tuning the model overfits, where  R2 reduced to 63 and RMSE increased to 0.184. The scores was unsatisfactory, So we decide to try LGBM(Light Gradient Boosting ) because these boosting tree models work quite well with numerical and continuous variables which is entirely what our dataset is.

* **LGBM** : We found that this gradient boosting model worked best and it gives an **R2 which is nearer to 93 and Adjusted R2 of 92**. LGBM is a whole model of decision trees which learns by fitting negative gradients which are called residual errors. LGBM has over 100 parameters but we have used only few which we found it necessary to prevent the model from overfit..Only small amount of time taken for its run when compared to Random Forest and also produced good result too..



