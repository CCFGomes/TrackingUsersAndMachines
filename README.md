# TrackingUsersAndMachines

1. Purpose:
 
- This project aims to create a Python script generating a daily report tracking user-machine interactions, specifically focusing on users logged in to respective machines at a given time.

Input:

- The input will be a list of events, with each event represented as an instance of the Event class. 
- Each event contains attributes such as the event date, the involved user, the machine's name, and the event type (login/logout).

Output:

- The generated report will display information regarding currently logged-in users for each machine, printed on the screen.

2. Research

- It's important to be clear on the parameters. To find out which users are currently logged into machines, we need to check when they logged in and when they logged out.
- If a user logged into a machine and then logged out, they're no longer logged into it. But if they didn't logout out yet, they're still logged in.
- It's vital that we process the events in chronological order
- For that we will have to sort the lists

3. Planning

- When processing each event, we'll maintain a dictionary to track users currently logged into each machine.
- The key-value pairs in the dictionary will represent each machine and its associated set of users.

Event Processing:

- For each event, we'll check if the machine is already recorded in the dictionary.
- If the machine is new, we'll create a new entry in the dictionary.
- If the machine already exists, we'll update the user set based on the event action (login/logout).
- Logging in will add the user to the set, while logging out will remove the user.

Dictionary Structure:

- The dictionary will use the machine name as the key and a set of users as the value.
- This structure ensures quick access to users logged into each machine.

Reporting Function:

- After processing the events, a separate function will generate the report.
- This function will receive the updated dictionary and print the machine names along with their respective logged-in users.

4. Writing the Python  Script

- You can find the Python Script in the files 'writingthescrip', and 'checkingthecode'
  
6. Generating the report

- You can find it in the file 'generatingreport'



