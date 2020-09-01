# Premier League Moneyball
##### Charles Peters - University of Nottingham 
##### Unviersity email: pmycp7@nottingham.ac.uk

#### Abstract
In modern day football, the deciding factor of which team wins the Premier League is often who has the most money. However, there is no 
point in having excessive amounts of money if it isnt being spent optimally. Inspired by the film "Moneyball", I wanted to develop my 
own program to determine how teams could build the best 25-man squad possible based on their payroll.

#### Data
I will use two websites to extract my data from:

* **sportrac.com/epl** - This website contains data on the payroll of every premier league team, and what wages each player is currently on.

* **premierleague.com/stats** - The official premier league website contains all the releveant statistics for every premier league player since 2006.
 
 The following modules will be used to extract the data into a jupyter notebook:
```
 import requests
 from bs4 import BeautfiulSoup
```

#### Overview
* I will start by fitting plots of different player statistics vs winrate. For example how a player's number of goals scored affects his win rate.
The players used in this initial stage will be selected randomly, but players will only be compared to other players in their position (i.e.
I will not be comparing the stats between attacking players and defensive players).
* A regression model can be developed to determine how different statistics have a greater influence on win rate. For example scoring more goals
may increase a player's winrate more than having a higher number of shots on target.
* The reason I want to determine how certain attributes affect win rate is because using win rate alone is not enough to judge a players value.
A weak player may have a high win rate simply because they play for a strong team and vice versa. 
* Thus my program will be able to detect players that have the attributes of a strong player, but have a lower win rate than expected (potentially due to
the team they play for).
* I will then develop a model which assigns a predicted win rate to each player. This is effectively the win rate you would expect a player to have based purely
on their individual statistics. The player with the highest predicted win rate is what the model regards to be the best player.
* These predicted win rates can then be compared to the players wages, indicating which players are better than their wages may suggest.
* The final goal is to write a function which builds a squad with the highest overall expected win rate that a given club can afford in wages.

* Only premier league players will be considered in this program. The reason for this is because there are millions of professional football players around the world,
and inlcuding players from other leagues would make the problem significantly more complex.
