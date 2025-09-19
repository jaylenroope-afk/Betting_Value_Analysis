# Betting Value Analysis for an Online Sportsbook

## Project Background
To ensure profitability, a sportsbook must make accurate predictions while offering competitive lines to online bettors. Sportsbooks can lose money if they fail to recognize when a player or team’s lines are consistently set above or below the actual outcomes. Therefore, in this project, I will analyze sportsbook data from the past five NBA seasons to identify trends in algorithmic predictions of popular NBA lines, such as the spread and points total.

## Tools and Skills Used
- Python (Pandas, Matplotlib, Seaborn, Data Sorting/Filtering, Dataframes, Visualizations)
- GitHub (Documentation, Reporting)

## Project Structure
- /README.md - What you are reading right now. This provides the description of the project, tools used, code, visualizations, and insights gained from the analysis.
- /[data](https://github.com/jaylenroope-afk/Betting_Value_Analysis/tree/main/data) - Contains the raw data gathered
- [1_code.ipynb](https://github.com/jaylenroope-afk/Betting_Value_Analysis/blob/main/1_code.ipynb) - Contains the Jupyter Notebook containing code used for the analysis
- /[visualizations](https://github.com/jaylenroope-afk/Betting_Value_Analysis/tree/main/Visualizations) - Contains matplotlib visualizations 

## Analysis Summary
In this analysis, I focused on points spread and total points as the two key performance indicators (KPIs) for a sportsbook company. Using data from the past six NBA seasons (2020–2025), the sportsbook’s algorithm improved its spread predictions over time, with the average points off the spread decreasing from 0.82 in 2020 to 0.14 in 2025. However, the algorithm generally overestimated the actual spread, with the exception of the 2021 season, where it slightly underestimated on average.

At the team level, the algorithm was least accurate for the Denver Nuggets (average overestimate of 1.42 points) and the OKC Thunder (average underestimate of -0.77 points), while it was almost perfect for the Golden State Warriors (-0.000969 points).

For total points predictions (the sum of points scored by both teams), the algorithm consistently underestimated totals, except in 2021, when it slightly overestimated by 0.01 points. The worst performance was in 2020, with an average underestimate of -1.09 points.

## Key Performance Indicators (KPIs)
### Points Spread Deviation 
- Measures how accurate the algorithm predicted the spread or difference in points between the favored team and the opposing team from 2020 (19-20) to the 2025 (24-25) NBA season.
- Analysis on seasonal trends as well as specific teams.

### Total Points Deviation 
- Measures how accurate the algorithm predicted the total points in a game which is the sum of the points from each team.

## Insights Deep-Dive
### Points Spread Analysis
![pts spread by season](https://github.com/jaylenroope-afk/Betting_Value_Analysis/blob/main/Visualizations/season_pts_spread.png)

*Points spread deviation from actual score difference from the 2019-2020 NBA season to the 2024-2025 NBA season*
- Algorithm has improved since the 2020 NBA season where the average points off the spread was 0.82 compared to 0.14 in 2025.
- In the past 6 NBA seasons, the algorithm consistently overestimated the spread except in the 2022 NBA season where it was off by -0.15 points.

![pts_spread_by_team](https://github.com/jaylenroope-afk/Betting_Value_Analysis/blob/main/Visualizations/avg_pts_spread_by_team_subplot.png)

*Subplots of teams where the spreads were either overestimated or underestimated*
- For the teams where the spread was overestimated, the algorithm was worst at predicting the spread for the Denver Nuggets (+1.42 pts), Sacramento Kings (+1.39 pts), and Los Angeles Lakers (+1.38 pts).
- For the teams where the spread was underestimated, the algorithm was worst at predicting the spread for the OKC Thunder (-0.77 pts), Memphis Grizzlies (-0.62 pts), Portland Trailblazers (-0.62 pts).
- The algorithm best predicted Golden State Warriors games with the points spread only being off by -0.000969 which is basically perfect.

![total pts dff by season](https://github.com/jaylenroope-afk/Betting_Value_Analysis/blob/main/Visualizations/season_total_pts_diff.png)

*Barchart of the total points deviation by season*
- Since 2020, the algorithm has consistenly underestimated the total points scored in a game, except in 2021 where it was about perfect in predicting the total points (+0.0012).
- There are no clear signs that indicate the algorithm has improved in predicting the point total, although 2020 had the worst total point prediction with an average difference of -1.09 while in 2025 it was only -0.75.

## Recommendations for the Sportsbook Company
### Spread
- Since the algorithm has consistently overestimated the spread, I recommend adjusting it slightly so that the predicted spread values are lower.
- Pay particular attention to teams where the predicted spread exceeds the actual by more than one point, such as the **Denver Nuggets, Sacramento Kings, LA Lakers, Minnesota Timberwolves, Indiana Pacers, and Atlanta Hawks**. From the bettor’s perspective, these teams may be recognized as consistently overestimated, leading bettors to choose the under, which can reduce the company’s profits. If this pattern is noticeable, the algorithm could be adjusted so that the **odds for the under are slightly less favorable**, encouraging bettors to pick the over instead.
- For teams whose predicted spread closely matches the actual outcome, the company could offer **promotional incentives**, such as bet multipliers, to encourage wagers on teams whose spreads are more difficult to predict, helping balance risk and engagement.

### Point Total
- Although the algorithm has predicted the total points within 1 point on average since 2020, the algorithm has consistently underestimated the total points scored in a game. Consider increasing the points total by about 0.5 points as the latest season was off by about -0.75 points.

## Limitations
- This project only looks at the point spread and point total lines in sportsbooks. There are many other betting props such as specific player lines that were not analyzed as the dataset did not provide lines on players.

## Datset
- Data was found on [Kaggle](https://www.kaggle.com/datasets/cviaxmiwnptr/nba-betting-data-october-2007-to-june-2024).
- Dataset was in one csv file containing 23118 rows and 27 columns of game data since 2008

