Acceptance testing ‘Van Halen Project’

- Legend –

Underlined items are system components

“Quoted lines are (printed) strings”


Case: As a user, I can create an account in order to use for logging into 
the web application.(ACC)



Instruction		
ACC_0.1	
Instruction
Type “User1” into the field Username. 
Type “Password1” into the field Password. 
Type “Password1” into the field Verify Password. 
Click on the button Create Account.
Expected Result
A new screen loads with the text “Account created”.	
Actual Result 	
Succes?

ACC_0.2	
Instruction
Leave the field Username empty. Type “Password1” into the field Password. Type “Password1” into the field Verify Password. 
Click on the button Create Account.	
Expected Result
A red prompt appears next to the Username field stating: “Please enter a username.”
Actual Result 	
Succes?

ACC_0.3	
Instruction
Type “User2” into the field Username. Type “Password1” into the field Password. Type “Password2” into the field Verify Password. 
Click on the button Create Account.	
Expected Result
A red prompt appears next to the Verify Password field stating: “Passwords do not match.”	
Actual Result 	
Succes?


ACC_0.4	
Instruction
Type “User2” into the field Username.  Leave the fields Password and Verify Password empty.
Expected Result
A red prompt appears next to the Password field stating: “Please enter a password.”		
Actual Result 	
Succes?


ACC_0.5	
Instruction
After creating account ‘User1’, type “User1” into the field Username. 
Type “Password1” into the field Password. 
Type “Password1” into the field Verify Password. 
Click on the button Create Account.	
Expected Result
A red prompt appears next to the Username field stating: “This username already exists, please choose another.”		
Actual Result 	
Succes?

 
Case: As a user, I can login to the web application in order to use the sorting machine. (INLOG)

		
INLOG_0.1	
Instruction
Type “User1” into the field Username. Type “Password1” into the field Password. Click on the Login button.	
Expected Result
A new screen loads with the application interface.
Actual Result 
Succes?

INLOG_0.2	
Instruction
Leave the field Username empty. Type “Password1” into the field Password. 
Click on the Login button.
Expected Result
A red prompt appears next to the Username field stating: “Please enter your username.”
Actual Result 
Succes?

INLOG_0.3
Instruction
Type “User1” into the field Username. Type “Password2” into the field Password. 
Click on the Login button.	
Expected Result
A red prompt appears next to the Password field stating: “Password incorrect.”	
Actual Result 
Succes?


INLOG_0.4	
Instruction
Type “Usser1” into the field Username. Type “Password1” into the field Password. Click on the Login button.
Expected Result
A red prompt appears next to the Username field stating: “This user does not exist. Please try again.”	
Actual Result 
Succes?




Case: As a user, I can start and stop the sorting process from the web interface
so that the sorting machine can be used safely. (STASTO)

		 	
STASTO _0.1	
Instruction
When the sorting process is inactive, click on the Sort button.	
Expected Result	
The sorting machine begins its sorting process based on the previously selected sorting pattern.
Actual Result
Succes?


STASTO _0.2	
Instruction
When the sorting process is active, click on the Stop button.	
Expected Result	
The sorting machine begins its sorting process based on the selected sorting pattern.	
Actual Result
Succes?


Case: As a user, I can pick colors in order to sort them according to my preferences. (COLSEL)

				
COLSEL _0.1	
Instruction
In the Color Selection menu, use the selection tool to pick a color.	
Expected Result
The screen displays “Sort all skittles of the [color] color?”.
Also displays a Sort Button and a Cancel button.
Actual Result 
Succes?



Case: As a user, I can sort all different colors to different containers.(SORTALL)

			
SORTALL _0.1	
Instruction
When the sorting process is inactive, click on the Sort button.
Expected Result
The sorting machine begins its sorting process based on the selected sorting pattern.	
Actual Result 
Succes?

SORTALL _0.2	
Instruction
When the sorting process is active, click on the Stop button.
Expected Result
The sorting machine begins its sorting process based on the selected sorting pattern.		
Actual Result 
Succes?


 
Case: As a user, I can enter an amount so that the sorting machine will stop
sorting once that number is reached. (AMOUNT)

			
AMOUNT_0.1	
Instruction
From the Sort All menu add a specific amount of total Skittles to be sorted.	
Expected Result
The machine should start sorting Skittles until the chosen amount is reached (or there are no mores Skittles left).		
Actual Result
Succes?


Case: As a user, I can enter an amount and color so that the sorting machine will stop sorting once the number
of the given color is reached. (AMOUNTCOL)

AMOUNTCOL_0.1	
Instruction
Once a color is selected, enter a specific amount of that color to be sorted and press the Sort button.	
Expected Result
The machine should start sorting Skittles until the chosen amount of the designated color is reached 
(or there are no mores Skittles left).		
Actual Result 	
Succes?


Case: As a user, I receive feedback from the system in order to monitor the status of the sorting job and the machine. (STATUS)

		
STATUS_0.1	
Instruction
When the system is not sorting, consult the Status readout. 
Expected Result	
Status readout reads “Idle”	
Actual Result 	
Succes?

STATUS_0.2	
Instruction
When the system is not sorting because there are no more Skittles, consult the Status readout.
Expected Result
Status readout reads “No Skittles available”. 	
Actual Result 	
Succes?

STATUS_0.3	
Instruction
When the system is sorting, consult the Status readout.
Expected Result
Status readout reads “Sorting”. A counter shows the count of the current amount of sorted Skittles.		
Actual Result 	
Succes?

Case: As a user, all my sorting data will be saved to a database so that it can 
be used for future reference including viewing my personal job history.(DATABASE)

		
DATABASE_0.1	
Instruction
Choose Previous Sorting Jobs from the main menu.	
Expected Result
All previously recorded sorting jobs are displayed, sorted by date.		
Actual Result 	
Succes?


DATABASE_0.2	
Instruction
From Previous Sorting Jobs select the results to view.  	
Expected Result
The parameters of the selected sorting job are displayed. These are:
•	User
•	Date/Time
•	Type of sorting
•	Chosen amount (if any)
•	Results	
Actual Result 	
Succes?


DATABASE_0.3
Instruction
From Sorting History, select My Sorting Jobs.	
Expected Result
All sorting jobs from the active account are displayed and can be selected to view results as with DATABASE_0.2		


Case: As a user, I can fill the sorting machine with Skittles in order for the sorting machine to user 
for the sorting jobs.(FILL)


		 	
FILL_0.1	
Instruction
When Status readout reads “No Skittles available”, open the Feeding container on the machine and add more Skittles. 
Expected Result
Once refilled Status readout reads “Idle”.		
Actual Result
Succes?

 

Case: The sorting machine will detect the Skittle to sort. (DETECT)

		 	
DETECT_0.1
Instruction
When a Skittle is available to scan while no job is active, check the  Status readout.
Expected Result
Status readout reads “Idle”.	
Actual Result
Succes?

DETECT_0.2	
Instruction
When a Skittle is available during a job and the Status readout reads “Sorting” check the Feeder mechanism.
Expected Result
The Feeder mechanism moves the Skittle to the Color scanner.	
Actual Result
Succes?


Case: The sorting machine will scan the color of given Skittle. (SCAN)
		
SCAN_0.1	
Instruction
When a Skittle is scanned, consult the Result Readout to see if the correct color is counted.
Expected Result	
The Color counter for the corresponding increases +1. 
Actual Result 	
Succes?

Case: The sorting machine will process one Skittle at a time. (SINGLE)
		
SINGLE_0.1	
Instruction
When a Skittle is moved from the Feeder mechanism to the Color scanner, look at the Color scanner.
Expected Result
The Scanning receptacle contains only one Skittle.  
Actual Result 	
Succes?

 
Case: The sorting machine will route the Skittle to the desired container (ROUTE)
	
ROUTE_0.1	
Instruction
When a Skittle is moved from the Color scanner to the container , look at the desired container.
Expected Result	
The scanned Skittle should be deposited in the correct container.  
Actual Result
Succes?		

Case: The system will alert a user if the connection between the interface and sorting machine is interrupted. (DISCONN)

	
DISCONN_0.1	
Instruction
When the user is logged in, sever the internet connection by unplugging the ethernet cable or shutting down the modem.	
Expected Result
Status readout reads “Connection interrupted.” All regular sorting options are disabled until the connection is restored.
Actual Result
Succes?
    

Case: The sorting machine will detect a full container and give feedback to the user. (FULL)
		
FULL_0.1	
Instruction
Fill a container to the ‘full’ mark. Look at the Status readout. 
Expected Result
The Status readout reads “Container full. Please empty container.”
All sorting options are disabled as with DISCONN_0.1 until container is emptied. 
Actual Result 
Succes?

FULL_0.2	
Instruction
Fill a container to just below the ‘full’ mark. Start a sorting job that would place another 20 Skittles 
into the designated container. Look at the Status readout. 
Expected Result
The system sorts the job as normal and displays current results.
When the container is detected as ‘full’, the sorting job stops and the Status readout reads 
“Container full. Please empty container.” 
Actual Result 
Succes?

# Integration
Integration test plan

Test 1 – Account Creation Check

Go to the create account screen at the **Frontend** and the Database at the **Backend** and enter the following tests.

| Test ID | Description | Expected Result | Actual Result | Succes? |
| --- | --- | --- | --- | --- |
| F\_ACC\_0.1 | In username type &quot;UserName1&quot;, in password type &quot;Password1&quot; and in emailtype &quot;dummy@fontys.nl&quot;. | The screen will confirm creation of account (&quot;Account created&quot;) and an entry of the user account info will be added to the Databasefile in the Backend. | |
|
| F\_ACC\_0.2 | After completing ACC\_0.1 reopen the create account screen. In username type &quot;UserName1&quot;, in password type &quot;Password1&quot; and in emailtype &quot;dummy2@fontys.nl&quot;. | The backend will verify that this username is already included in the Database and trigger an error message for the frontend. The screen will show an error message &quot;This username is already taken, please try again&quot;. | |
|
| F\_ACC\_0.3 | After completing ACC\_0.1 reopen the create account screen. In username type &quot;UserName2&quot;, in password type &quot;Password1&quot; and in emailtype &quot;dummy@fontys.nl&quot;. | The backend will verify that this email is already included in the Database and trigger an error message for the frontend. The screen will show an error message &quot;This email adress is already taken, please try again&quot;. | |
|

Test 2 – Account Login Check

Go to the login screen at the **Frontend** and the Database at the **Backend** and enter the following tests.

| Test ID | Description | Expected Result | Actual Result | Succes? |
| --- | --- | --- | --- | --- |
| F\_AL\_01 | Correct data is entered in the fields and the login button is pressed | The login menu goes away. And you will be redirected to another page |
 |
 |
| F\_AL\_02 | The right Login Name is entered in the login field, but the wrong password | There is an error showing, that the login name is incorrect |
 |
 |
| F\_AL\_03 | The wrong Login Name is entered in the login field, but the right password | There is an error showing, that the password is incorrect |
 |
 |
| F\_AL\_04 | The wrong Login Name is entered in the login field, but the wrong password | There is an error showing, that the login name is incorrect |
 |
 |

Test 3 – Current Skittle Count Check

Go to the sorting request screen at the **Frontend** and the Database at the **Backend** enter the following tests.

| Test ID | Description | Expected Result | Actual Result | Succes? |
| --- | --- | --- | --- | --- |
| F\_CSCC\_0.1 | While the sorting request screen is active, check the number of available skittles under the color Yellow.Go to the Backend and open the Databaseand check the amount of Skittles under the color Yellow. | Both Skittle counts have the same amount of available Skittles under the color Yellow. |
 |
 |
| F\_CSCC\_0.2 | While the sorting request screen is active, check the number of available skittles under the color Red.Go to the Backend and open the Databaseand check the amount of Skittles under the color Red. | Both Skittle counts have the same amount of available Skittles under the color Red. |
 |
 |
| F\_CSCC\_0.3 | While the sorting request screen is active, check the number of available skittles under the color Purple.Go to the Backend and open the Databaseand check the amount of Skittles under the color Purple | Both Skittle counts have the same amount of available Skittles under the color Purple. |
 |
 |
| F\_CSCC\_0.4 | While the sorting request screen is active, check the number of available skittles under the color Green.Go to the Backend and open the Databaseand check the amount of Skittles under the color Green | Both Skittle counts have the same amount of available Skittles under the color Green. |
 |
 |
| F\_CSCC\_0.5 | While the sorting request screen is active, check the number of available skittles under the color Orange.Go to the Backend and open the Databaseand check the amount of Skittles under the color Orange | Both Skittle counts have the same amount of available Skittles under the color Orange. |
 |
 |

Test 4-Order Skittles

Go to the sorting request screen at the **Frontend** and the Database at the **Backend** enter the following tests

| Test ID | Description | Expected Result | Actual Result | Succes? |
| --- | --- | --- | --- | --- |
| F\_OS\_01 | All the selectors are correctly filled in (greater than zero), then we press ok | A JSON message goes to the backend with the correct amount of chosen skittles. |
 |
 |
| F\_OS\_02 | An incorrect JSON string is send from the frontend to the backend | The backend gives you a warning that the JSON string send is not correct |
 |
 |
| F\_OS\_03 | Backend does not respond to the send message (no connection). | The message should be saved for when the connection comes back online. After that the backend should redo the request. |
 |
 |

Test 5 –Skittle Count Check After Sort

Go to the Database at the **Backend** and the sorting reservoir at the **Arduino** , and enter

| Test ID | Description | Expected Result | Actual Result | Succes? |
| --- | --- | --- | --- | --- |
| B\_SCCAS\_0.1 | At the Database check and note the current amounts of Yellow skittles at each color.Then take two (2) Yellow Skittles, add them to the sorting reservoir of the Arduino sorter. Start the Arduino sorting process. After the process is finished, check and note the current amount of Yellow Skittles at the Database | The amount of Yellow Skittles has incremented by two (2). |
 |
 |
| B\_SCCAS\_0.2 | At the Database check and note the current amounts of Red skittles at each color.Then take two (2) Red Skittles, add them to the sorting reservoir of the Arduino sorter. Start the Arduino sorting process. After the process is finished, check and note the current amount of Red Skittles at the Database. | The amount of Red Skittles has incremented by two (2). |
 |
 |
| B\_SCCAS\_0.3 | At the Database check and note the current amounts of Purple skittles at each color.Then take two (2) Purple Skittles, add them to the sorting reservoir of the Arduino sorter. Start the Arduino sorting process. After the process is finished, check and note the current amount of Purple Skittles at the Database. | The amount of Purple Skittles has incremented by two (2). |
 |
 |
| B\_SCCAS\_0.4 | At the Database check and note the current amounts of Green skittles at each color.Then take two (2) Green Skittles, add them to the sorting reservoir of the Arduino sorter. Start the Arduino sorting process. After the process is finished, check and note the current amount of Green Skittles at the Database. | The amount of Green Skittles has incremented by two (2). |
 |
 |
| B\_SCCAS\_0.5 | At the Database check and note the current amounts of Orange skittles at each color.Then take two (2) Orange Skittles, add them to the sorting reservoir of the Arduino sorter. Start the Arduino sorting process. After the process is finished, check and note the current amount of Orange Skittles at the Database. | The amount of Orange Skittles has incremented by two (2). |
 |
 |

the following tests.

Test 6 –Skittle Count Check After Order

| Test ID | Description | Expected Result | Actual Result | Succes? |
| --- | --- | --- | --- | --- |
| SCCAO\_0.1 | While the sorting request screen is active, check and note the number of available Yellow Skittles. Enter an order of two (2) Yellow Skittles and click the order button.After the order has been sorted, check and note the number of available Yellow Skittles again.Check the order receptacle of the Arduino. | The amount of available Yellow Skittles at the sorting request screen has decreased by two (2).The order receptacle at the Arduino now holds two (2) Yellow Skittles. |
 |
 |
| SCCAO\_0.2 | While the sorting request screen is active, check and note the number of available Red Skittles. Enter an order of two (2) Red Skittles and click the order button.After the order has been sorted, check and note the number of available Red Skittles again.Check the order receptacle of the Arduino. | The amount of available Red Skittles at the sorting request screen has decreased by two (2).The order receptacle at the Arduino now holds two (2) Red Skittles. |
 |
 |
| SCCAO\_0.3 | While the sorting request screen is active, check and note the number of available Purple Skittles. Enter an order of two (2) Purple Skittles and click the order button.After the order has been sorted, check and note the number of available Purple Skittles again.Check the order receptacle of the Arduino. | The amount of available Purple Skittles at the sorting request screen has decreased by two (2).The order receptacle at the Arduino now holds two (2) Purple Skittles. |
 |
 |
| SCCAO\_0.4 | While the sorting request screen is active, check and note the number of available Green Skittles. Enter an order of two (2) Green Skittles and click the order button.After the order has been sorted, check and note the number of available Green Skittles again.Check the order receptacle of the Arduino.
 | The amount of available Green Skittles at the sorting request screen has decreased by two (2).The order receptacle at the Arduino now holds two (2) Green Skittles. |
 |
 |
| SCCAO\_0.5 | While the sorting request screen is active, check and note the number of available Orange Skittles. Enter an order of two (2) Orange Skittles and click the order button.After the order has been sorted, check and note the number of available Orange Skittles again.Check the order receptacle of the Arduino. | The amount of available Orange Skittles at the sorting request screen has decreased by two (2).The order receptacle at the Arduino now holds two (2) Orange Skittles. |
 |
 |

Go the sorting request screen at the **Frontend** and the order receptacle of the **Arduino** , then enter the following tests.

Test 7-Account validation

??

| Test ID | Description | Expected Result | Actual Result | Succes? |
| --- | --- | --- | --- | --- |
| B\_AV\_01 | The back-end should sent a token when the account is correctly validated | When a Login request from is coming in from the front-end. Check the given data. When approved the backend send an approval back to the frontend |
 |
 |
| B\_AV\_02 | The back-end should throw an error when wrong username is send. | When a Login request from is coming in from the frond-end, check the given data.If the username does not exist. The backend should throw an error back to front-end. |
 |
 |
| B\_AV\_03 | The back-end should throw an error when a wrong password is send. | When a Login request from is coming in from the frond-end, check the given data.If the password does not match the given username. The backend should throw an error back to front-end saying the. |
 |
 |

Test 8-Sorted Skittles - back-end

Go to the Database at the **Backend** and the sorting reservoir at the **Arduino** , and enter

the following tests

| Test ID | Description | Expected Result | Actual Result | Succes? |
| --- | --- | --- | --- | --- |
| B\_SK\_01 | The backend should store the sorted values of the color when the MQTT server sends a JSON text. | When the JSON string is acquired. The backend should store the given values in a list. |
 |
 |
| B\_SK\_02 | When incorrect data is send from the MQTT server. The back-end should respond with a message. | When the incorrect data is catched. The backend should return a message to the frontend that something went wrong. |
 |
 |
| B\_SK\_03 | When a request from the front-end comes to get the correct amount of skittles left. The backend makes a get request to the MQTT server to give the data, and sends that data back to the front-end | The data send by the MQTT server is stored in a repository. This data is send via JSON to the front-end who then stores it in the amount available on the page. |
 |
 |

Test 9-Sorted Skittles – Arduino

??

| Test ID | Description | Expected Result | Actual Result | Succes? |
| --- | --- | --- | --- | --- |
| A\_SK\_01 | When the sorting machine has finished sorting. Data needs to be send to an MQTT Server. | When finished sorting. The Arduino sends the values to an MQTT server who then waits from a request from the backend to get the information. |
 |
 |
| A\_SK\_02 | When the servo motor is not running so that the machine stops sorting. That information has to be stored into a logfile | As soon as the machine stops working via a busted servo. A log file should be updated or created. |
 |
 |
| A\_SK\_03 | When there are no skittles left to be sorted. There should be a message saying the bin is empty. | As soon as the machine detects there are no more skittles left to sort. A message needs to be send to the backend informing the problem. |
 |
 |
