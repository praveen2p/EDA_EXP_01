### Name : PRAVEEN K
### Reg.No: 212223040152

## Experiment 1: EDA in IPL Dataset
## Aim:
To perform Exploratory Data Analysis (EDA) on the IPL matches dataset and derive insights about matches per season, winning teams, toss decisions, and top venues.

## Algorithm / Procedure:

## 1.Import Libraries
  Import pandas for data handling.
  Import matplotlib and seaborn for visualization.
  
## 2.Load Dataset
  Use pd.read_csv() to load the IPL matches dataset.
  Check dataset shape using .shape.
  View first 5 rows using .head().
  
## 3.Matches per Season (Univariate Analysis)
  Group data by season and count matches.
  Plot a bar chart to visualize growth/decline in matches.
  
## 4.Top Winning Teams (Univariate Analysis)
  Use value_counts() on the winner column.
  Plot top 5 winning teams in a bar chart.
  
## 5.Toss Decisions (Univariate Analysis)
  Count toss decision preferences (bat vs field).
  Plot results using a bar chart.
  
## 6.Top Venues (Univariate Analysis)
  Count matches per venue.
  Display top 5 venues with a horizontal bar chart.
  
## 7.Draw Insights
  Observe patterns in toss decisions.
  Identify teams with consistent winning trends.
  
  
  ## Program
  ## 1.Dataset Structure  ( find the uploaded dataset matches.csv)
  How many rows and columns are present in the dataset?
  What does the first 5 rows of data look like?
  ```
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
df=pd.read_csv('matches.csv')
df.head()


df.shape

 ```

  ## Output
  <img width="986" height="612" alt="image" src="https://github.com/user-attachments/assets/f1b62a38-0aaf-490a-b546-a28adde471e0" />
<img width="465" height="127" alt="image" src="https://github.com/user-attachments/assets/504f02be-9716-4ecf-a4cc-82ffc51810d3" />

## Matches per Season

How many matches were played in each IPL season?
Can we visualize the trend of matches across seasons?

```
matches_per_season = df['season'].value_counts().sort_index()
matches_per_season
import matplotlib.pyplot as plt

matches_per_season.plot(kind='line', marker='o')
plt.xlabel("Season")
plt.ylabel("Number of Matches")
plt.title("Matches Played per IPL Season")
plt.show()

```
## Output:
<img width="735" height="655" alt="image" src="https://github.com/user-attachments/assets/68fc3d09-2fcc-4887-8f8a-6b18a179f03c" />
<img width="967" height="601" alt="image" src="https://github.com/user-attachments/assets/336354f5-f0c6-4417-bb45-861064b0d3fb" />

## Top Winning Teams

Which teams have won the most matches overall?
Can we plot the top 5 winning teams?

```
top_teams = df['winner'].value_counts()
top_teams
top_5_teams = top_teams.head(5)

top_5_teams.plot(kind='bar')
plt.xlabel("Team")
plt.ylabel("Matches Won")
plt.title("Top 5 Winning IPL Teams")
plt.show()



```

## Output:
<img width="833" height="664" alt="image" src="https://github.com/user-attachments/assets/36aa5adf-72cd-4e48-9faf-e3d7754e9336" />
<img width="851" height="698" alt="image" src="https://github.com/user-attachments/assets/301cb509-ad25-4a95-9d8a-07f704c8b7e2" />


## Toss Decisions

What do captains usually choose after winning the toss (bat or field)?
Can we show this preference in a bar chart?

```
toss_decision = df['toss_decision'].value_counts()
toss_decision

toss_decision.plot(kind='bar')
plt.xlabel("Toss Decision")
plt.ylabel("Count")
plt.title("Toss Decision Preference")
plt.show()
```

## Output:
<img width="531" height="262" alt="image" src="https://github.com/user-attachments/assets/fb3486a1-b499-4eb8-8827-df7ecfae94c8" />
<img width="843" height="537" alt="image" src="https://github.com/user-attachments/assets/cdefe94b-6fad-4f5d-850c-7fc33e4a5147" />


## Top Venues

Which stadiums have hosted the most matches?
Can we display the top 5 venues in a clear visual?

```
top_venues = df['venue'].value_counts()
top_venues.head(5)

top_venues.head(5).plot(kind='bar')
plt.xlabel("Venue")
plt.ylabel("Number of Matches")
plt.title("Top 5 IPL Venues")
plt.show()


```

## Output:

<img width="637" height="415" alt="image" src="https://github.com/user-attachments/assets/d4bd9e11-c5b1-4e94-8eb1-b716b5db35ee" />
<img width="926" height="684" alt="image" src="https://github.com/user-attachments/assets/aead04dd-07c4-4846-af12-a3206194117d" />


 ## Result
  This experiment is executed successfully.




