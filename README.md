# Data Incubator Application
Thank you for reviewing my Data Incubaor Application.

This repo is aiming  to provide all the code and content for my Data Incubator challenge including the questiones and the project.

Challenge Questions File:
The answers for Section 1 (Baltimore Parking Citations) and section 2 (Kinight Moves) are available here.

Below is my project propal, you could find my code and plot in the project file.

# DotA2 Win Probability Prediction Based on Hero Lineups
## Introduction and Motivation:
My project is aiming to use logistic regression and neural network to predict the winning side of a DotA2 based on hero lineups. DotA2 is a very popular game. A regular DotA2 match has ten players with five players on each side. Each player will choose a hero from 118 heroes and try to defeat their opponents. Every hero is unique and can make a vital contribution to the victory, therefore, I decided to try to use only hero lineups to predict the winning side at this moment. 

I have been playing DotA for more than 10 years and I still love it. Dota is a very complex game and I am excited that I would combine my data analysis skills with my passion and knowledge for  DotA to drive some useful conclusion and bring some innovative insights and inspiration to millions of players.  
## Data Collection:
Thanks for Opendota which is the largest open source DotA2 platform, I used their API to retrieve all the data I need. Due to the restriction of the API, I found 100 random high skill matches first. Then I recorded all the player IDs in those matches and find their recent matches. By doing so, I ensured that most of the matches are high level and evenly distributed of all the games, therefore my conclusion would not be biased and can provide some constructive advice.

Due to the API calls rate limit, I can only retrieve the data of around 5000 matches until now but they are enough for me to get some conclusion. The data of a match include how long the match is, what heros are selected in the match, which team wins the game and so much more.  

## Exploratory data analysis：
Since each DotA2 game has two sides, one is “Radiant” and the other is “Dire”, the first thing I calculate is the winrate of each side. The DotA2 map is not symmetrical, yet there are only little difference between each side, people just assumed the winrate to be fifty-fifty. However, based on my calculations, ‘Radiant’ has 58.6% win rate which is 17.2% higher than the ‘Dire’ Team, which is absolutely not inconsiderable.  

There are 118 heroes in the game, of course some of them are popular among players but are they as powerful as people think? I sorted heroes’ pick rate to found the 15 most popular heroes and calculate their winrate. It is shocking that the most popular hero, ‘Magnus’, who was picked 35 times in 50 matches, had only less than 9% win rate in high level games.   

I also took a look at the relationship between heroes and the duration of the games. In my opinion, if a hero presents often in long games, then they either has weak attack ability or strong defense ability.   

## Logistic Regression and Prediction:
I defined the feature vector as a (1⨯236) vector. The first half of the feature vector represents the ‘Radiant’ side while the second half of the feature vector represents the ‘Dire’ Side. Xi=1  means that a player plays hero i. I label each match with Y=1 if ‘Radiant’ won, Y=0 if ‘Dire’ won. I used logistic regression on the data set. I split 70% of the matches as training set and others as the test set. The test accuracy is around 80% which I am pretty satisfied.  

## Future Work:
There is a bunch of interesting facts hiding under the data. I could use the Gold Difference and XP Difference between each team to measure the advantage or disadvantage a team has, then I could find which heroes have the largest potential to make a comeback and which heroes are the most powerful in the early game.  

I could also add more features to the logistic regression model such as heroes countering or synergy. I am also planning to try Neutral Network or add more in-game features to make real time prediction.  

I would also working on heroes selection recommendation system, which will provide advice for players' next pick based on what heroes both teams have chosen.
