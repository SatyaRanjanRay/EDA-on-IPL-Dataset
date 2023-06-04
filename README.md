# EDA-on-IPL-Dataset
Exploratory Data Analysis on IPL Dataset🏏
IPL Overview
The Indian Premier League (IPL) is a men's Twenty20 (T20) cricket league that is annually held in India and contested by ten city-based franchise teams.The IPL is the most-popular cricket league in the world; in 2014, it was ranked sixth by average attendance among all sports leagues. In 2010, the IPL became the first sporting event to be broadcast live on YouTube.

According to BCCI, the 2015 IPL season contributed ₹1,150 crore (US 140 million dollars) to the GDP of the economy of India. According to a report by consulting firm D & P Advisory, In December 2022, the IPL became a decacorn valued at 10.9 Billion dollars, registering a 75percent growth in dollar terms since 2020 when it was valued at 6.2 billion dollars. IPL 2023 final was the most streamed live event on internet with 3.2 Cr viewers.
## Content
In the following nb, I have performed Exploratory Data Analysis on IPL Dataset.

Necessary columns used from the Dataset :
season: consists the year when the tournament was held
city: consists the city where the matches were played
team1 & team2: consists both the teams of each matches
toss_winner: consists the name of the team who won the toss
result: consists the result of the match
dl_applied: consists whether Duckworth-Lewis method was applied to a match or not
winner: consists Winner of the match
win_by_runs and win_by_wickets: consists winning stats
player_of_match: consists MOM info
venue: consists the name of stadiums where matches were played

## Analysis
This includes the Analysis on Match informations,Team Statistics,City and Venue details, Toss decision to field or bat,effect of toss on the outcome of the match, Match results etc.

- No of Matches played in each season
- No of Matches played in each city and Venue
- No of Matches won by each team in total and in each season
- Win stats either by runs or wickets
- Toss wins and Toss decisions
- No of Matches where Duckworth-Lewis was applied
- Match results (Normal/Tie)
- Player of the Match Award

## Steps for EDAs:
- Import the necessary libraries
- Load the data using pandas and explore the data
- Data cleaning and Preparation
- Exploratory Analysis and Visualisations
- Conclusion and recommendations

### Question1
No of Matches played in each season

A new dataframe called `No_of_matches` is created which has two columns: "Year" and "Matches". The "Year" column is created using 'value_counts()' method on the "season" column of the `df` dataframe. The 'index' attribute of this series is used to create the "Year" column of the new dataframe. The "Matches" column is created using 'values' attribute of the series which contains the count of each unique value in the "season" column.
Using the new dataframe along with "Year" and "Matches" columns as labels, A barplot is plotted for the visualisation.

### Question2
No of Matches played in each city and venue

A city series is created using 'value_counts()' method on the "city" column of the df dataframe.
A barplot is plotted using 'index' and 'values' attribute of the city series as labels.
Another barplot is plotted using 'index' and 'values' of the venue series as lables.

### Question3
No of Matches won by each team in total and in each season

A countplot is plotted using "winner" column and 'value_counts()' method on the "winner" column of the df with 'index' attribute.

A Function is defined named bar_plot which is called while visualizing No of matches won by each team in each year.

### Question4
Win Stats by runs or wickets

A histplot is plotted to visualize the distribution of Winning by runs.
Wins by Top5 teams who opted to bat first is visualized by the help of a barplot using "value_counts()" method along with 'index' and 'values' attribute on the "winner" column.

A histplot is plotted to visualize the distribution of winning by wickets.
Wins by Top5 teams who opted to bowl first is visualized by the help of a barplot using
"value_counts()" method along with 'index' and 'values' attribute on the "winner" column.

Different functions (named batting_first,batting_second) is defined for both the analysis and called when needed.

### Question5
Toss Wins and Toss Decisions

Toss wins by each team is visualized using barplot using 'index' and 'values' attribute of "toss_winner" series.

Toss Decisions to bat or field is visualized using donut (pie) chart and Toss Decisions in each IPL season is visualized using countplot.

### Question6

Different Scenarios for match outcomes such as "Was toss winner also the match winner",
"No of matches where DL applied" and "Match results was normal or tie" is visualized using the pie chart for better understanding.

### Question7
Player of the match is visualized by Barplot using "player_of_match" column attributes

## Conclusion
* From the Analysis It has been found that Most no of matches were played in the year 2013 whereas In Mumbai Most of the matches were played but M Chinnaswamy stadium,Bangalore was the venue for most of the matches.
* Mumbai Indians won the most number of matches (92) followed by Kolkata Knight Riders (77) and Chennai Super Kings (77) between the year 2008-2017.
* Mumbai Indians has won most matches when batted first (47) followed by Chennai Super Kings (45). Kolkata Knight Riders has won the most matches when batted second (46) followed by Mumbai Indians (44).
* Mumbai Indians has also won more tosses (83) followed by Kolkata Knight Riders (77).
* It also has been found that Toss winning team prefered fielding over batting. Field (57%) and Bat (43%). Also 2016 was the year when most of the teams chose to field.
* The Match winning percentage of Toss winning teams were 51% and for only 2.5% of matches the DL Rule was applied due to bad weather conditions and also the Match was ended as a tie for 1.12% of total matches.
* Chris Gayle is the most awarded Player of the match (18)
