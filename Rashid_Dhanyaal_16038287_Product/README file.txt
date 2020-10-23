How to run the program and how it works:
How to import the project to eclipse and android studio:
1: Open eclipse ide version and make sure you have got tomcat 8.5 downloaded. 
2: If you have got different tomcat version, you can change the configurations in eclipse. 
3: Next, go to file and then go to import archive file.
4: Next click browse, and this will now direct you to the directory, where you would need to go to the directory where the files have been saved.
5: Next, make sure it's zip file and not uncompressed file. Then, click finish and it should appear in your eclipse without any errors. 
6: Now, you should be able to run the eclipse project successfully without any problems/errors.

Opening/importing android application in android studio:
1: In order to open/import the android project into android studio, make sure the file has been uncompressed first.
2: Next, go to file open.
3: This should now direct you to the directory, here you should pick the directory where the file has been saved.
4: Next, once you have got to the directory, click ok and it should add the project to your android studio. 
5: Now, you should be able to run both the eclipse project and android project successfully. 
6: For the blind’s activity page, you would need to run the rfid dao class first each time as the connection closes often. NOTE don't think this is an error which is not, its common as the connection closes each time. Once, the motor subscriber has been run, you would then be able to run the application and the data will then be added to the database. 

Eclipse project using valid tag and invalid tag:
1: Connect both the rfid reader and interface kit to the laptop.
2: Connect the sensors to the interface kit on 2 different channels.
3: Set the channel in the code to the correct channel where the sensors are plugged into.
4: Run the rfid dao (server class).
5: Run the rfidlight class first on the java application to test the sensor works.
Scan valid tag, if valid tag has been used the light will turn on. Otherwise, if invalid tag has been used, the light won’t turn on.
6: Test the temperature client class on java application. 
7: Scan valid tag, if valid tag has been used the heating will turn on. Otherwise, if invalid tag has been used, the heating won’t turn on.
8: Test the rfid blinds client class on java application. 
9: Scan valid tag, if valid tag has been used the blinds will open. Otherwise, if invalid tag has been used, the blinds won’t open, and the motor won't move.
10: All the data will also be sent to the server/database as json string and be viewed on the browser in json format.

Android app:
Valid credentials:
Email: dh11any@hotmail.com
password: dhani7865

1: Run the application on android studio.
2: Type in the valid credentials, e.g. email and password and then press sign in. This will now direct you to the main app page, where you can control the light, heating’s and blinds.
3: Press the light on button, this will then check if valid tag has been used or not. If valid tag has been used, the light will turn on.
4: Next press heating on button, this will now direct you to another page where you will be able to control the heating’s.
5: Press the heating on button. This will now turn the heating’s on, if valid tag has been used.
6: Go back to the main app page and press the open blinds button. This will now open the blinds and move the motor, if valid tag has been used. Also, make sure the motor subscriber class has also been run, as well as the rfid dao. The data will also be sent to the server/database. 
7: Notification will be sent to the mobile device letting you know if the light is on/off, heating’s on/off or if the blinds are opened/closed.
8: If wrong credentials have been used in the log in form. It won’t allow the user to log into the application. It will only allow 3 goes to type in valid email and password. As part of 
the security. After 3 attempts have been used it will then direct you back to the log in page to type in valid email and password.

All messages will be published to the correct topic.
Mqtt is the protocol which has been used.

Main activity – The light data will be published to the topic_rfid.
Heating activity – The heating and temperature data will be published to the topic_temperature.
Blinds activity – The blinds data will be published and subscribed to the topic_motor. 
