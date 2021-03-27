# election-analysis

## Project Overview
In this hypothetical scenario, I am assisting a Colorado Board of Elections employee with an audit of the tabulated results of an election for a U.S. Congressional district in Colorado. This project uses Python programming language to access, process, manipulate, and store data from a .csv file in order to automate the vote-counting process. The .csv data source includes the ballot ID, county, and candidate for each vote in the election. 

The use of for loops and conditional statements with membership and logical operators were used to calculate the election results. The results were then printed to the command line and saved in a text file for delivery of the analysis. 

The Colorado Board of Elections employee provided the following tasks to complete:

1. Calculate the total number of votes cast.
2. Get a complete list of candidates who received votes.
3. Calculate the total number of votes each candidate received.
4. Calculate the percentage of votes each candidate won.
5. Determine the winner of the election based on popular vote.
6. Calculate voter turnout for each county.
7. Calculate the percentage of votes from each county out of the total count.
8. Determine the county with the highest turnout.

## Resources
- Data Source: election_results.csv
- Software: Python 3.8.5; Visual Studio Code 1.54.3

## Results
The analysis of the election shows that:
- There were 369,711 votes cast in the election.
- Votes were collected from the following counties:
  - Jefferson
  - Denver
  - Araphoe
- County turnout results and their percentage of the total vote count were:
  - Jefferson: 38,855 (10.5%)
  - Denver: 306,055 (82.8%)
  - Arapahoe: 24,801 (6.7%)
- The county with the highest turnout was Denver
- The candidates were:
  - Charles Casper Stockham
  - Diana DeGette
  - Raymon Anthony Doane
- The candidate results were:
  - Charles Casper Stockham received 23.0% of the vote and 85,213 number of votes.  
  - Diana DeGette received 73.8% of the vote and 272,892 number of votes.  
  - Raymon Anthony Doane received 3.1% of the vote and 11,606 number of votes.  
- The winner of the election was:
  - Diana DeGette, who received 73.8% of the vote and 272,892 number of votes.

## Summary of Future Use Cases
Election commission officals can now redeploy this [code](https://github.com/tysonseang/election-analysis/blob/main/PyPoll_Challenge.py) to calculate election outcomes across the state. The code requires that the source files follow the same formatting structure to execute properly. If the data source is not in the same format, two pieces of code need to be adjusted. 

Firstly, the appropriate depenencies and file paths will need to reflect the appropriate file type, file name, and file location of the new data source and text file output. The use of a .csv source file would be the easiest implementation. File paths and file names will still need to be updated in the code. This section is shown below.

```
# Add our dependencies.
import csv
import os

# Add a variable to load a file from a path.
file_to_load = os.path.join("Resources", "election_results.csv")
# Add a variable to save the file to a path.
file_to_save = os.path.join("analysis", "election_results.txt")
```

Secondly, the index numbers that pull results for county_name and candidate_name will need to be updated to reflect their position in the new data source.   

```
# Get the candidate name from each row.
candidate_name = row[2]

# Extract the county name from each row.
county_name = row[1]
```
Mirroring the format of the election_results.csv file with same column order of Ballot ID, County, and Candidate would prevent any required code updates here. 
