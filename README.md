# Overview of Election Audit
This analysis was conducted in order to parse a CSV file of local election data and find how many votes were cast and received by counties and candidates respectively, and ultimately determine who the winning candidate was.  While this project could have been done in Excel, Python code was used instead to both automate the process and to allow it to be more easily extrapolated to different and larger districts where Excel could potentially struggle with bigger data sets.

# Election-Audit Results
Over the course of this analysis, the following results were found regarding the election data.
*  369,711 votes were cast in total.  
*  Arapahoe County cast 24,801 votes, which amounted to 6.7% of the total
*  Jefferson County cast 38,855 votes, which amounted to 10.5% of the total
*  Denver County cast the largest number of votes at 306,055, which amounted to 82.8% of the total
*  The candidate Raymon Anthony Doane received 11,606 votes, which amounted to 3.1% of the total
*  The candidate Charles Casper Stockham received 85,213 votes, which amounted to 23.0% of the total
*  The candidate Diana DeGette won the election with 272,892 votes, which amounted to 73.8% of the total

In order to find these results, after using a “With” statement to load the CSV file, a “For” loop was used to iterate through and count every row to first find the total number of votes.  Included was a line of code to make sure the script did not count the headers as a vote.  Then, the “For” loop was coded to add each unique county name and candidate name it found to lists, as well as adding votes associated with each county and candidate to dictionaries.  A calculation was written to draw the number of votes from these dictionaries and compare it to the total number of votes in order to find each county and candidate’s percentages, and finally a “Print” statement was used to display the results.

# Election-Audit Summary
Once this code was written it was able to return the desired results nearly instantly, despite being required to read over 300,000 lines of data.  This is much faster than a method like Excel would have been able to accomplish the task, and can be used much more easily on different data sets where more than only three candidates and counties are being tracked.  Were this script to be used on larger scale elections, the code may need to be modified to add further lists and dictionaries accounting for more fields of interest like districts or states.  Additional modifications would then be necessary to add vote counts to those dictionaries within the “For” loop in order to be able to print percentages and vote numbers for districts or states.
