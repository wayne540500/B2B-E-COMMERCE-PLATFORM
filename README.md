# B2B-E-COMMERCE-PLATFORM

About the project
The Business to Business(B2B) E-commerce Platform is a simplified graphical user interface
(GUI) application designed for furniture store clerks. It enables them to manage
customer/user account registration and checking, calculate and display the user's current
order(product quantity and total price) in the shopping cart, and send the purchase order
as a text file to the factory server for manufacturing, shipping, and credit card charging
purposes. We have implemented a database to handle user account checks and
registrations and established a TCP socket connection to send and store purchase order
text files on the factory server's desktop. The B2B e-commerce platform application is using
the MVC architecture pattern that separates an application into three main logical
components: the model, the view, and the controller. Each of these components are built
to handle specific development aspects of an application. MVC is one of the most
frequently used industry-standard web development frameworks to create scalable and
extensible projects.

![image](https://github.com/wayne540500/B2B-E-COMMERCE-PLATFORM/assets/69573286/b534af58-2033-46dc-8657-9af1ac49ffe7)

MVC Overview:

![image](https://github.com/wayne540500/B2B-E-COMMERCE-PLATFORM/assets/69573286/58867d41-6d4d-4e56-86c0-160e7c0daa81)

Demo Video
https://youtu.be/kVEsGiZewy8

![image](https://github.com/wayne540500/B2B-E-COMMERCE-PLATFORM/assets/69573286/ccd11e0c-0ee7-43ca-aa90-6fc703a6daa8)

Database Setup
To run this project, we need to set up a MySQL database to store the information of our customer in the table. If a new customer does not have an account and wants to register a new account, it will save the new customer’s name and password to our database at the same time, and show Register Successful!. Else if the name and password already existed, it will show User Name Already Exist! And for customers who already have the account just simply type in your login info if successful it will show Login Successful ! , else if a customer types wrong user name or wrong password it will show User Not Found, Please Register or Wrong Password ! 

![image](https://github.com/wayne540500/B2B-E-COMMERCE-PLATFORM/assets/69573286/cbc952df-47f4-4f1b-a010-30bff98912a3)
![image](https://github.com/wayne540500/B2B-E-COMMERCE-PLATFORM/assets/69573286/17cd395f-501f-4b93-afe7-962a63fd47e0)

For the mysql connector google mysql connector and download it, then right click on the project-properties-Build Path-Library, add externals JARs to your library :

![image](https://github.com/wayne540500/B2B-E-COMMERCE-PLATFORM/assets/69573286/cf88af52-2b3b-40cc-b23e-da6676748d89)

MySQL Workbench

![image](https://github.com/wayne540500/B2B-E-COMMERCE-PLATFORM/assets/69573286/a0536ebf-73df-4ad0-bfa0-cfbbf382a05c)

Server Connection
For the server part we create a Factory Server, every time when a new client tries to place an order from our platform. The server will receive a .txt file which contains  the information of our customer ( including: Package Receiver, Address, City… ) and save the text file on its desktop; Moreover, if a customer successfully submits the order it will show Submit Order Successfully! otherwise Submit Order Fail!. When Factory Server receives the .txt file of the customer the factory can start producing, packaging, and shipping products according to the customer information from the .txt file.
Following are the command to setup the Factory Server on MacOS Terminal before running the B2B E-commerce Platform:
Factory Server Command:
1.)	 cd /Users/Jerry/eclipse-workspace/finalProject/src/application/
2.)	 javac FactoryServer.java
3.)	 cd ..
4.)	 java application.FactoryServer

![image](https://github.com/wayne540500/B2B-E-COMMERCE-PLATFORM/assets/69573286/026f40f1-1b89-4b21-899d-b338c35244bc)

In FactoryServer.java please change desktopPath to your corresponding path, in order to receive client’s order:

![image](https://github.com/wayne540500/B2B-E-COMMERCE-PLATFORM/assets/69573286/2f89e1e3-64a0-4f20-98ee-a0bdc443b9e3)

![image](https://github.com/wayne540500/B2B-E-COMMERCE-PLATFORM/assets/69573286/65b11765-7a67-4c2a-ab01-3652b78b11cd)

JavaFX
In eclipse java marketplace download the following:

![image](https://github.com/wayne540500/B2B-E-COMMERCE-PLATFORM/assets/69573286/0b42a177-bfa1-423e-93a3-91bd73093f1a)

And then google JavaFX download platform-specific SDK :

![image](https://github.com/wayne540500/B2B-E-COMMERCE-PLATFORM/assets/69573286/52673770-e17a-4fc2-a740-f2b2421c6e03)

Then go to preference-Java-Build Path add external JARs:

![image](https://github.com/wayne540500/B2B-E-COMMERCE-PLATFORM/assets/69573286/cb092779-5fbe-4f2d-b739-896bf59fa8ba)

Then right click on the project go to Build Path-Configure Build Path-Library-Add Library-User Library, add JavaFX into our library:

![image](https://github.com/wayne540500/B2B-E-COMMERCE-PLATFORM/assets/69573286/a2f128f5-b3e3-439a-872d-a710d713d5fd)

Finally, right click on the project go to run as configuration- argument, add this line in the blank then click apply:

![image](https://github.com/wayne540500/B2B-E-COMMERCE-PLATFORM/assets/69573286/7ff31cfc-d64d-4485-9b8c-c6a1ba56df94)

How to Use
It is quite straightforward to use our Business to Business (B2B) E-commerce platform, once you start the program. You will see the login/registration part, shopping cart and our products. 
First, run the FactoryServer.java to start the server.
Second, run the Main.java, if you don’t have an account just simply create one, else if you already have one just type in your account and password. Our database is able to determine whether the user has an account or not.
Third, add the items you want to purchase, our shopping cart will show you the total amount, and if you decide to place the order just simply press the place the order button and fill in the payment info. If you place your order successfully our server will receive your order, otherwise you will receive a submit order fail message.
Finally, our server will receive your order and generate a txt file including your order details and information.
As a reminder: for the chair image usage, please change the path of product1.jpg to corresponding path in lobby.fxml

![image](https://github.com/wayne540500/B2B-E-COMMERCE-PLATFORM/assets/69573286/07dbadf2-dcb5-4b0f-b6ea-efd2f2ea5585)
