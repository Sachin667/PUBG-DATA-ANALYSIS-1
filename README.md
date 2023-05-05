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
