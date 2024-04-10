### Project Proposal - 100+ Years of Baseball Statistics
Andrew Moore - Friday, March 22, 2024

### Project Overview  
Baseball is a favorite among sports statisticians, due in part to the wealth of data going back to the mid-1800s. Sports statistics, and especially baseball statistics, are something I have been interested in since I was young, and they are one of the main reasons I took an interest in data science and statistics. This dataset specifically interests me because I think it is an ideal size for me to learn memory management in pandas. It is large enough (~1Gb when loaded into a dataframe with default options) for me to learn how to deal with large datasets, but small enough that I can still carry out the analysis I want to if the learning curve for memory management is too steep for me to carry it out effectively. I think this dataset also lends itself well to a large variety of visualizations, leaving me plenty of options.


#### Dataset  

**MLB game logs (1871-2023)** Game logs contain 161 data columns for each regular season game played in the MLB from 1871-2023, ~200,000 rows. The dataset contains box score and traditional statistics aggregated by team per game. It has data on the umpires present at the game, and all the players on each side. It also contains day of the week, home and visiting teams, day/night, attendance, and stadium information.  

[https://data.world/dataquest/mlb-game-logs](https://data.world/dataquest/mlb-game-logs) - The game logs for 1871-2016 converted into a convenient csv format with named columns.  
[https://www.retrosheet.org/gamelogs/index.html](https://www.retrosheet.org/gamelogs/index.html) - Raw game logs for 1871-2023. I will use the raw data for 2017-2023 to complete the 1871-2016 dataset. There is also playoff game and world series log data here I may use. Finally, it contains detailed column info and ballpark codes.  

**Player and Statcast Data** If I want more advanced statistics for modern games or stats aggregated by player, season, or team, this resource will serve as an easily accessible database for this information.  

[https://github.com/jldbc/pybaseball](https://github.com/jldbc/pybaseball) - pybaseball is a python package built to aggregate data from these sources:  

- [https://www.mlb.com/statcast](https://www.mlb.com/statcast), [https://www.fangraphs.com](https://www.fangraphs.com), [https://www.baseball-reference.com](https://www.baseball-reference.com)

#### Data Analysis   
    
**Home Field Advantage**  
- How significant is home field advantage?  
- Do specific teams or stadiums have more significant home field advantages?  
- Did American League have an home field advantage over National League teams or vice versa when the DH rule was different?

**Umpire Effects**  
- Do specific home plate umpires have effects on pitching stats?  
- Do specific umpires favor specific teams?  

**Baseball Scorigami**  
"Scorigami" is a popular topic in football, where many strange scores are possible. Each time a never before seen score occurs in football, it is known as "scorigami." Applying this topic to baseball:  
- Are there any reasonable score we would expect to see that we have never witnessed?  
- How does the score distribution look over time?  

**Baseball Over Time**  

- How have hitting and pitching stats changed over time?  
- How has game length changed over time? Has the newly implemented pitch clock worked?  
- Do games or seasons cluster on offensive or pitching statistics? If I perform unsupervised clustering, can we annotate these clusters with eras in baseball (dead-ball era, steroid era, etc.)?

**BONUS (if I have time): Player Network Analysis**  

- What does a network graph look like for all players in the dataset?  
- Do players with a lot of node connections correspond with high-profile figures in baseball?  

#### Methods and Timeline       
  
**Data Preprocessing, Cleaning, and Memory Management**: 1-2 weeks, finish by April 7.  

- Finish dataset by adding 2017-2023 data, pandas.   
- Handle nan values for important fields, pandas.  
- Optimize memory usage of dataframe, pandas.  
  
**Data Preparation**: 1.5 weeks, finish by April 20.  

- Create dataframes for each data analysis section. pandas, numpy.   
- Pull additional data if needed. pybaseball.  
  
**Data Modeling and Visualization**: 2 weeks, finish by May 3.  

- Temporal data. matplotlib, seaborn.  
- Heatmaps (Scorigami). seaborn, plotly.  
- Violin plots, scatter plots, swarm plots. seaborn.  
- Unsupervised clustering using Density-Based Spatial Clustering of Applications with Noise (DBSCAN). scikit-learn.  
- BONUS (if time): network graph. networkx, plotly.  
