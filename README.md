# Election_Analysis

##Challenge Overview
I completed an analysis of an election audit to determine which county in Colorado had the largest voter turnout.
1.	Got a complete list of counties that had votes casted.
2.	Calculated the total number of votes for each county.
3.	Calculated the percentage of the total votes each county received.
4.	Determined which county had the largest voter turnout.

### Resources
Data Source: election_results.csv
Software: Python 3.7.6, Visual Stuido Code, 1.54.3

####Election-Audit Results
The analysis of the election audit shows that:
•	There were 369,711 votes casted in the Colorado election.
•	The counties were:
  o	Jefferson
  o	Denver
  o	Arapahoe
•	The county results were:
  o	Jefferson received 38, 855 votes for 10.5% of the total votes
  o	Denver received 306,055 votes for 82.8% of the total votes
  o	Arapahoe received 24,801 votes for 6.7% of the total votes
•	The county with the largest number of votes casted was:
  o	Denver with 306,055 votes casted

•	Example of the loop I used to pull the data:
##### 6a: Write a for loop to get the county from the county dictionary.
    for county_name in county_votes:
        # 6b: Retrieve the county vote count.
        county_total_votes = county_votes[county_name]
        # 6c: Calculate the percentage of votes for the county.
        county_percentage = float(county_total_votes) / float(total_votes) * 100

        # 6d: Print the county results to the terminal.
        county_results = (f"{county_name}: {county_percentage:.1f}% ({county_total_votes:,})\n")
        print(county_results)
        # 6e: Save the county votes to a text file.
        txt_file.write(county_results)
        # 6f: Write an if statement to determine the winning county and get its vote count.
        if (county_total_votes > biggest_county_count):
            biggest_county_count = county_total_votes
            biggest_county = county_name

    # 7: Print the county with the largest turnout to the terminal.
    biggest_county_summary = (
        f"-------------------------\n"
        f"Largest County Turnout: {biggest_county}\n"
        f"-------------------------\n")
    print(biggest_county_summary)

    # 8: Save the county with the largest turnout to a text file.
    txt_file.write(biggest_county_summary)

•	The candidate results were:
  o	Charles Casper Stockham received 23.0% of the vote and 85,213 number of votes.
  o	Diana DeGette received 73.8% of the votes and 272,892 number of votes.
  o	Raymon Anthony Doane received 3.1% of the votes and 11,606 number of votes.
•	The winner of the election was:
  o	Diana DeGette won the election with 73.8% of the votes and 272,892 votes.
###### Election-Audit Summary
In summary I believe my script can help with the election audit in any of the upcoming elections by modifying it to see which age group or which ethnicity is casting the most votes. If I was provided more detail from the ballot like the age and race of the person who casted the vote, I can give a detailed break down to see who is coming out to vote and we can even take that detail down to the county level as well.
