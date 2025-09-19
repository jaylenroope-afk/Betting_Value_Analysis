# Betting Value Analysis for an Online Sportsbook

## Project Background
To ensure profitability, a sportsbook must make accurate predictions while offering competitive lines to online bettors. Sportsbooks can lose money if they fail to recognize when a player or team’s lines are consistently set above or below the actual outcomes. Therefore, in this project, I will analyze sportsbook data from the past five NBA seasons to identify trends in algorithmic predictions of popular NBA lines, such as the spread and points total.

## Tools and Skills Used
- Python (Pandas, Matplotlib, Seaborn, Data Sorting/Filtering, Dataframes, Visualizations)
- GitHub (Documentation, Reporting)

## Project Structure
- /README.md - What you are reading right now. This provides the description of the project, tools used, code, visualizations, and insights gained from the analysis.
- /data - Contains the raw data gathered
- 1_code.ipynb - Contains the Jupyter Notebook containing code used for the analysis
- /visualizations - Contains matplotlib visualizations 

## Analysis Summary
In this analysis, I used the points spread and total as my two KPIs I will be analyzing for the sportsbook company. Taking data from the past 6 NBA seasons (2020-2025), the sportsbook improved its algorithm in predicting the spread where the average points off spread was 0.82 in the 2020 NBA season and 0.14 in 2025. However, the algorithm tends to overestimate the actual spread. In this range, the 2021 season was the only season where the algorithm on average underestimated the spread. When looking at specific teams specifically for the spread, the algorithm was worst at predicting the spread for the Denver Nuggets with an average points off spread of 1.42 (overestimate) and OKC Thunder of -0.77 (underestimate). It was about perfect in predicting the spread for Golden State Warriors games (-0.000969). For the total points prediction, which is the sum of the points of the two teams in a game, the algorithm consistently underestimated the point total except in 2021 where it overestimated by an average of 0.01 points. In 2020, the algorithm was off by -1.09 points on average which was the worst year in this range. 

## Key Performance Indicators (KPIs)
### Points Spread Deviation 
- Measures how accurate the algorithm predicted the spread or difference in points between the favored team and the opposing team from 2020 (19-20) to the 2025 (24-25) NBA season
- Analysis on seasonal trends as well as specific teams 

### Total Points Deviation 
- Measures how accurate the algorithm predicted the total points in a game which is the sum of the points from each team.

## Insights Deep-Dive
### Points Spread Analysis
![pts spread by season](season_pts_spread.png)

