Robotic arm control system - arm control.
The system allows the user to change the values of 6 engines that are used in the robotic arm and run the arm or stop it. Furthermore, it allows the user to view the current values of the engines and the status of the arm (On / Off). The values are stored in a MySQL database.
Description of files:

index.php file:
This is the main page of the website, and it displays 6 sliders that have the range (0-180) and 3 buttons:
1.Save: To store the new values of the engines.
2.Run / Stop: To change the status of the device.
3.Show current values: To show the current values in a table. 
Initially when the page is loaded, the current values of the engines are retrieved from the database and shown in the range slider.

sliderValue.js file:
This JavaScript file displays the current value of the slider in real time.
startConnection.php file:
This file is used to connect to the database and is used to avoid repetition in the code.

run.php file:
This page is opened when clicking “Run” / “Stop” / “Show current values” buttons. 
When “Run” / “Stop” is clicked, the status of the device is changed accordingly. The table of the current values is displayed afterwards. Moreover, there is “Go back” button which when clicked redirects the user to “index.php” page.

Design of the database:
There is 1 table that has 7 columns. For each engine there is one column and an extra column used to store the current status of the device as Boolean. If the status is on, the value is true, otherwise it is false. The website uses only one row and updates it each time a new value is changed.

How to run the files:
-Download XAMPP or any equivalent software to run MySQL and PHP.
-Import the database “robotarmcontrol.sql”.
-Open “startConnection.php” file and change the values of the variables “$servername”, “$username”, “$password”, and “$dbname” according to your settings.	
