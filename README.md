# FantasyPLSpreadsheet-Forecasts-FixtureTicker-ScorelinePrediction-Solver
An Excel spreadsheet for FantasyPL. It calculates player attacking form, and team attacking and defending form at home and away from past data. This is then used to create a fixture ticker and player attacking forecasts based on form and fixtures. In the FixtureTicker sheet there is a scoreline predictor, which takes the distribution of attacking scores in the fixture ticker, and transforms it to the 2019-20 xG distribution. Gameweek 0 data refers to GW20-38 of 2019/20. Player data is per start. Promoted teams are assumed to have the worst attacking and defending data, it will take a while for forecasts involving them to be reliable.

In PlayerForm and TeamForm there are cells you should change that are filled in light blue/cyan. These are the metric weightings, which change the proportion of 'underlying' stats that make up form. There is the next gameweek cell, which is currently set to 1. There is also the scale factor cell, which gives you the option of giving more recent gameweeks more importance in calculating form. This is currently set to 1.25. A value of 1 gives all gameweeks equal importance, as you go above 1, recent gameweeks are given more importance. Below 1, recent gameweeks are given less importance, which is not recommended. 

Solver - I probably will not use this much as I would prefer to pick players looking at Graphs, being able to see their price points.
1. This is currently set to solve the best attack for the next 6 gameweeks.
2. Change the cells filled in light blue/cyan based on your intuition.
3. These are the constraints for the amount of players from a team, budget spent on goalkeepers, how many defenders you would like to start (from 3 to 5), and exclusions and inclusions.
4. For example you may want to pick a maximum of 2 players from Chelsea, and you may want to pick a minimum of 1 player from Manchester United for whatever reasons you may have.
5. PlayerIDs for exclusion and inclusion can be found in the PlayerData sheet.
6. You must include your 5 defenders of choice.
7. If you want to include a new player, add their information at the bottom of the player list in the Solver, and include them in the inclusion list. 
8. You may need to sort column I (6GW Forecast) in the PlayerForecast sheet by largest to smallest, after adding exclusions.
