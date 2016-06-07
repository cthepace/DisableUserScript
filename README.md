# DisableUserScript
written by: Dipesh Bhattarai
Date: 01/06/2016

-Searches user based on either their first name, last name or their login id.
		-List the users that matches the search and display their First Name, Last Name and their Department
-Disable user from active directory
				1. Remove user from all the groups.
							-copy all groups that user was assigend to notes: 
							- add disabled date to notes
				2. Hide user from Global Address Book.
							-set external and internal OOO
							-hide user from address book
				3. Disable user:
							-disable user account
							-move to To be <DELTED FOLDER>.
	


<#Usage
Type User's first Name and Last Name or  User Name to find the user and follow the prompt:

eg: if you want to delete "JANE JONES"..
1. Enter First and Last Name. This is the default mode. You do not have to type full name(s). It takes partial texts too.

.\Disable-HPUser.ps1 -FirstName JANE -LastName JONES
.\Disable-HPUser.ps1 -First Name "JA" -lastname "JO"

This will search AD with the above names and list the user matching above inputs in their first and last Name.



2. You can pass other parameters as well. eg

.\Disable-User.ps1 -firstn Jane -lastn jones -oooexternal="<text to set as ooo external>" -ooointernal= "<text to set as internal>" 

3. search can also be performed using username instead:

.\Disable-User.ps1 -loginname jjones



Searches for User with above initial string in their names.
#>
