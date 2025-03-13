# IPL_data_analysis_tasks

**Overview**
------------

This project performs data analysis on an IPL dataset containing ball-by-ball details of matches. Various insights are extracted, including top scorers, highest totals, umpire statistics, and team performances.

**Datasets**
-----------
### dataset1: df1
The dataset contains columns such as:

1.   `id`: Match ID
2.   `inning`: Inning number
3.   `over`: Over number
4.   `ball`: Ball number
5.   `batsman`: Name of the batsman
6.   `non_striker`: Name of the non-striker
7.   `bowler`: Name of the bowler
8.   `batsman_runs`: Runs scored by the batsman
9.   `extra_runs`: Extra runs conceded
10.   `total_runs`: Total runs scored in the delivery
11.   `is_wicket`: Indicates if the batsman got out
12.   `dismissal_kind`: Type of dismissal
13.   `player_dismissed`: Name of the dismissed batsman
14.   `fielder`: Name of the fielder involved in dismissal
15.  `batting_team`: Batting team name
16.  `bowling_team`: Bowling team name

### Dataset: df2

1.  **id** - Unique match identifier
2.  **city** - City where the match was played
3.  **date** - Date of the match
4.  **player\_of\_match** - Player who was awarded "Man of the Match"
5.  **venue** - Name of the stadium where the match was played
6.  **neutral\_venue** - Indicates if the match was played at a neutral venue (0 = No, 1 = Yes)
7.  **team1** - Name of the first team
8.  **team2** - Name of the second team
9.  **toss\_winner** - Team that won the toss
10.  **toss\_decision** - Decision made after winning the toss (`bat` or `field`)
11.  **winner** - Team that won the match
12.  **result** - Type of result (`runs`, `wickets`, `tie`, etc.)
13.  **result\_margin** - Margin of victory (by runs or wickets)
14.  **eliminator** - Indicates if it was an eliminator match (`Y` or `N`)
15.  **method** - DLS method used (if applicable)
16.  **umpire1** - Name of the first on-field umpire
17.  **umpire2** - Name of the second on-field umpire

* * *

**Tasks Performed**
-------------------

### **1\. Total Number of Matches Played**

Counted the number of unique match IDs.

### **2\. Total Number of Runs Scored**

Summed up all `total_runs` to get the overall runs scored in IPL.

### **3\. Average Runs Scored per Match**

Calculated as:

Average Runs\=Total RunsTotal Matches\\text{Average Runs} = \\frac{\\text{Total Runs}}{\\text{Total Matches}}Average Runs\=Total MatchesTotal Runs​

### **4\. Umpire with the Highest Number of Matches Officiated**

Identified the umpire who has officiated the most matches.

### **5\. Team with the Most Toss Wins**

Found the team that won the most tosses.

### **6\. Team with the Highest Win Percentage**

Computed win percentage using:

Win Percentage\=(Total WinsTotal Matches Played)×100\\text{Win Percentage} = \\left(\\frac{\\text{Total Wins}}{\\text{Total Matches Played}}\\right) \\times 100Win Percentage\=(Total Matches PlayedTotal Wins​)×100

### **7\. Venue Where RCB Won Most Matches**

Determined the stadium where RCB has won the most matches.

### **8\. Highest Total Score in an Inning**

Identified the highest score by a team in a single inning.

### **9\. Highest Run-Scorer**

Found the player with the highest cumulative `batsman_runs` in the dataset.

`highest_scorer = df.groupby('batsman')['batsman_runs'].sum().idxmax()
highest_runs = df.groupby('batsman')['batsman_runs'].sum().max() print("Highest run-scorer:", highest_scorer) print("Total runs scored:", highest_runs)` 

* * *

**Requirements**
----------------

*   Python 3.x
*   Pandas
*   NumPy
*   Jupyter Notebook / Any Python IDE

* * *

**How to Run the Project**
--------------------------

1.  Install dependencies:
    
    `pip install pandas numpy` 
    
2.  Load the dataset into a Pandas DataFrame.
3.  Run the analysis scripts to extract insights.

* * *

**Author**
----------

*   **Kalpanil Kanbarkar**
*   **kalpanil22kanbarkar@gmail.com**
*   **Date: March 2025**

* * *
