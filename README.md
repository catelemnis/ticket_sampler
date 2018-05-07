# ticket_sampler
Program takes in a CSV listing of team-assigned tickets. It selects a random sample of the tickets, proportionate to how many tickets each user completed. It then assigns those tickets back to the team members for review, ensuring no user is assigned their own ticket.

README Created 20170927 Angelee Schmidt.

Modified 20180323 by Angelee Schmidt.

Created for Python 2.7.

2 reference files must be named:
	
	USERS.txt  = list of users that work on tickets 
	EVALUATORS.txt = list of people that will perform ticket evaluations


Input file must be a CSV Report.
Required headers:
	
	number
	resolved_at
	assigned_to
	work_notes


The CSV report must be in same folder as the script. Pass the name as the first argument.
Optional second argument is the percent size that the sample will be (in whole number, not decimal).

Ex.
	
	\>python evaluation_sampler_v2.0.py SN_REPORT.csv
	\>python evaluation_sampler_v2.0.py SN_REPORT.csv 20 #this will grab 20% sample of tickets from SN_REPORT.csv
	\>py -2 evaluation_sampler.py SN_REPORT.csv
