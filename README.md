# Election_Analysis
## Election Audit Overview
The purpose of the project was to complete an audit of a recent Colorado Congressional district election. The audit required me to tabulate county-level election results as well as the candidate vote totals, and finally the winner of the election. To complete this analysis, I created a script in Python to tabulate the election results from a CSV file. The full results of the audit can be found in ![election_analysis](analysis/election_analysis.txt)
## Election Audit Results
The election audit shows that:
- There were 369,711 votes cast in the election
Because each line of the CSV file represented a unique ballot, it was easy to collect the total number of votes by looping through the data and iterating the total number of votes. 
- The county results were:
  - Jefferson County accounted for 10.5% of the total vote for the district and 38,855 votes.
  - Denver County accounted for 82.8% of the total vote for the district and 72,892 votes.
  - Arapahoe County accounted for 3.1% of the total vote for the district and 24,801 votes.
To collect county-level results, the sript first extracts the county name from each line of the CSV file and uses those values to create a list of counties. The script then adds a vote for each instance of that county, and records the value in a dictionary.
```
county_name = row[1]
if county_name not in counties:
  counties.append(county_name)
  county_votes[county_name] = 0
county_votes[county_name] += 1
```
- County with the highest number of votes:
  - Denver County, with 72,892 votes.
To identify the county with the most votes, the script uses an if statement to compare the results from each county, setting the highest vote total to a variable. The highest number of votes is set as ```top_county_votes``` and the corresponding county is set to ```top_county```.
- The candidate results were:
  - Charles Casper Stockholm received 23% of the vote and 85,213 votes.
  - Diana DeGette received 73.8% of the vote and 272,892 votes.
  - Raymond Anthony Doane received 3.1% of the vote and 11,606 votes.
- The winner of the election was Diana DeGette with 73.8% of the vote and 72,892 votes.
The script tabulates candidate results with the same method it uses to get county-level vote totals. Candidate names and vote totals are stored their own lists and dictionaries, but the same logic is used to calculate the correct results.

## Election Audit Summary
The script created for this audit can easily be used for any first-past-the-post election. It can tabulate results for variable numbers of candidates and counties and can seemlessly tabulate results for other Congressional elections or state-wide races. The script can also easily be adapted to other types of elections. Local elections, for example, may not require county results. For those races, the code that collects county vote totals could be excluded. The script can also be modified to collect additional information, such as candidate party affiliation. The script is versatile and adaptable, making it an ideal foundation for audits of future elections at all levels.
