# Election_Analysis
## Election Audit Overview
The purpose of the project was to complete an audit of a recent Colorado Congressional district election. The audit required me to tabulate county-level election results as well as the candidate vote totals, and finally the winner of the election. To complete this analysis, I created a script in Python to tabulate the election results from a CSV file. The full results of the audit can be found in ![election_analysis](analysis/election_analysis.txt)
## Election Audit Results
The election audit shows that:
- There were 369,711 votes cast in the election

- The county results were:
  - Jefferson County accounted for 10.5% of the total vote for the district and 38,855 votes.
  - Denver County accounted for 82.8% of the total vote for the district and 72,892 votes.
  - Arapahoe County accounted for 3.1% of the total vote for the district and 24,801 votes.
- The candidate results were:
  - Charles Casper Stockholm received 23% of the vote and 85,213 votes.
  - Diana DeGette received 73.8% of the vote and 272,892 votes.
  - Raymond Anthony Doane received 3.1% of the vote and 11,606 votes.
- The winner of the election was Diana DeGette with 73.8% of the vote and 72,892 votes.
## Election Audit Summary
The script created for this audit can easily be used for any first-past-the-post election. It can tabulate results for variable numbers of candidates and counties and can seemlessly tabulate results for other Congressional elections or state-wide races. The script can also easily be adapted to other types of elections. Local elections, for example, may not require county results. For those races, the code that collects county vote totals could be excluded. The script can also be modified to collect additional information, such as candidate party affiliation. The script is versatile and adaptable, making it an ideal foundation for audits of future elections at all levels.
