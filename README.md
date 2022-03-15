# Chegg-People-Dashboard
People Dashboard along with backend API which has basic user management functionalities
Front-End : Angular Framework
Back-End : Java API using Gradle

Front-End: 
Setup:
•	Unzip the front-end.zip file 
•	Open PATIENT-DASHBOARD in the Visual Studio Code IDE(preferred) or any IDE of  choice.
•	How to Install and Set Up Angular on Windows 10 (zeolearn.com) 
Angular - Setting up the local environment and workspace– install Node JS and Angular JS by following the instructions in the given links.
•	In the terminal navigate to the src folder and run the following commands to start the angular server.
npm start (or) ng serve
Also run the following commands to install necessary dependencies if it shows any error like module not found.
	npm install -g @angular/cli
	npm install -g @angular/core
	npm install -g @angular/material
	npm install -g @angular/common
•	The server will start in localhost:4200
•	Try accessing localhostL4200 from browser of your choice and people dashboard will be displayed.
Front End code is written in typescript using the angular framework.  A basic people dashboard is designed which is has basic functionalities like add, update, delete, list and filter users. Below are the snapshots of the dashboard images.
Dashboard:
 ![image](https://user-images.githubusercontent.com/27359588/158313569-7c6f85ce-fd4b-4af5-b162-f84f82299354.png)




Add User: On clicking Add user button in the top right corner of dashboard will pop up a dialog box to populate user data.
![image](https://user-images.githubusercontent.com/27359588/158313597-827d5489-00f6-44e7-a545-5f83a06edafb.png)

 
Delete User:  - delete user is implemented using id. ID of the particular user which needs to be deleted has to be entered.
 ![image](https://user-images.githubusercontent.com/27359588/158313616-caafb6a6-46fb-42c5-9d1a-4c28cae21eab.png)










Search user: It gives two select options to choose school name and targeted user
 
 ![image](https://user-images.githubusercontent.com/27359588/158313626-cd4c54f2-0a01-46c7-bda5-d6120bbf2078.png)
![image](https://user-images.githubusercontent.com/27359588/158313635-1f8e121a-447f-4ee7-9a78-9ef0b7fecad1.png)


API: (server)
The APIs which are accessed by the above client is implemented in Java API using Gradle and all the APIs are unit tested using Junit framework
Folder structure:
•	src is the folder which contains the code
•	src-> main has implementation of the APIs
•	src -> test has Junit test cases
•	build.gradle – all the dependencies are mentioned in this file.


 ![image](https://user-images.githubusercontent.com/27359588/158316249-6739f5e3-9b9d-47ee-b477-9d6000bdda26.png)



Steps:
•	Unzip NivishreeBookstoreRest.zip file
•	Open the unzipped folder in IntelliJ(preferred) or any other browser of your choice.
•	Setup and run local Tomcat server
o	Go to the down arrow near the top right of IntelliJ. It says "Edit configurations..." when you click it. Click the [+] button at the top left and choose Tomcat -> Local. Name the configuration "Tomcat". The bottom of the dialog box should give a warning saying that no artifacts are marked for deployment. Click [Fix it] using [Name]BookstoreRest.war and give the application context the name /[Name]BookstoreRest. And give the URL to be http://localhost:8080/Chegg . (Refer the below image for reference and replicate it)



 ![image](https://user-images.githubusercontent.com/27359588/158316227-f4f4fa45-34e3-4948-b586-c77047554a1c.png)


•	Go to the File -> Project Structure -> Global Libraries click the + button and add path of lib lib folder in NivishreeBookstoreRest->dependencies


 ![image](https://user-images.githubusercontent.com/27359588/158316214-020e43ad-d28d-409d-afe2-28817648ae1f.png)

•	Start the server by click the green play button in the top right corner
•	The server should start in https://localhost:8080/Chegg
•	And the APIs can be accessed by http://localhost:8080/Chegg/api/*
o	Example: http://localhost:8080/Chegg/api/search/Student/All
If any error due to libraries or dependencies occurs then all the required jar files are in 
NivishreeBookstoreRest -> dependencies folder. Add the necessary jar files to the class path to resolve the dependency errors

List of API Path:
http://localhost:8080/Chegg/api/student - POST

http://localhost:8080/Chegg/api/search/Student/All - GET

http://localhost:8080/Chegg/api/search/Professor/All - GET

http://localhost:8080/Chegg/api/search/Student/{school-name} - GET

http://localhost:8080/Chegg/api/search/All/{school-name} - GET

http://localhost:8080/Chegg/api/search/Professor/{school-name} - GET

http://localhost:8080/Chegg/api/users - GET

http://localhost:8080/Chegg/api/professors - GET

http://localhost:8080/Chegg/api/students - GET

http://localhost:8080/Chegg/api/delete/{id} - DELETE

http://localhost:8080/Chegg/api/update/{lastName} - PUT


![image](https://user-images.githubusercontent.com/27359588/158316198-e2c860bc-1cca-4e06-ac29-1361cafc9ee7.png)

