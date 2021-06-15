# HippoCrypt-Database

The HippoCrypt-Database is a Flask web application system which provides a robust and highly secure banking system that secures user data and maintains user privacy through encryption algorithms and following hippocratic principles. The system is based on concepts of [CryptDB](https://dl.acm.org/doi/10.1145/2043556.2043566) and [Hippocratic Databases](https://doi.org/10.1145/2894750). A major focus of this project goes in ensuring that the web application provides customer with maximum authority over their personal data. Hippocratic principles empowers the users by providing the right to select the amount of shared information. Rules and regulations are set to limit the data that can be gathered, analyzed and retained by the companies. It also requires companies to provide complete disclosure of how the customer data is used and for what purpose. 

The entire database was encrypted using the Advanced Encryption Standard (AES) encryption with the help of Python scripts. AES is a symmetric block cipher that provides high speed and relatively high security in terms of bits.

An example snapshot of the encrypted data in our proposed system

![image](https://user-images.githubusercontent.com/46695666/121989945-f5437b80-cd6a-11eb-82a2-d96dacfecac1.png)

## Software Requirements

1) Python 3
2) Pycharm
3) MySQL

## Installation

1) Start MySQL command line and run bank_database.sql script
2) Start Pycharm and open "Server" folder as project
3) Go to Run - > Edit Configurations -> FlaskServer
4) Add user name and password of MySQL database separated by space in parameters field
5) Run FlaskServer.py file
6) To Open home page go to : http://127.0.0.1:5000/ Or Open file homePage.html click on "Go to Home Page"

## Navigating through the application (Customer)

### Home Page:

URL - http://127.0.0.1:5000/

- For first time users, click on Create an Account for signing up. 
- Select the account type (Customer) and enter the username and password and hit sign in.  

Sample Username: nihal Password: 123 Account type: Customer

![image](https://user-images.githubusercontent.com/46695666/121986930-77c93c80-cd65-11eb-9e74-639c4da0a9c8.png)

### Signup Page:

Fill in your personal details and then select account type (Business if the account belongs to a company or else select Individual). 

**Please check out the terms and conditions page**

![image](https://user-images.githubusercontent.com/46695666/121987009-99c2bf00-cd65-11eb-9ad3-6d480ea425fd.png)

![image](https://user-images.githubusercontent.com/46695666/121988130-ca0b5d00-cd67-11eb-8630-b158a7ac36ad.png)

After you click on the submit button, the application redirects to the home page where you can login using your newly created account credentials.

### Account Home Page:

Account Number, Balance and recent transactions can be viewed here. Click on Transfer option in upper right corner to go to Transfer page. Click on MyInfo option to view, update and delete personal data stored in the system.

![image](https://user-images.githubusercontent.com/46695666/121988337-19518d80-cd68-11eb-8d5c-d46f942c0db5.png)

### Transfer Page:

Select operation to perform and enter amount to be deposited or withdrawn. Click on Account home to go back to previous page

![image](https://user-images.githubusercontent.com/46695666/121988457-59187500-cd68-11eb-9217-dff3b6159bd0.png)

### View Info Page:

This page shows personal information stored with bank. Click on Account home to go back to previous page.

![image](https://user-images.githubusercontent.com/46695666/121988533-7ea57e80-cd68-11eb-90c0-2d822105681f.png)

### Update Info Page:

Select fields which you would like to update and enter the corresponding values to modify personal information. Click on Account home to go back to previous page.

![image](https://user-images.githubusercontent.com/46695666/121988620-aac0ff80-cd68-11eb-9a30-cbfe0eb006e8.png)

### Delete Info Page:

Select fields which you would like to delete and click on delete button to remove personal information. Click on Account home to go back to previous page.

![image](https://user-images.githubusercontent.com/46695666/121988687-cb895500-cd68-11eb-8163-2ed540d15203.png)

## Navigating through the application (Employee/Admin)

### Creating admin accounts:

Open createAdmin.py file in Server folder. Edit values of id, password, and role and run the file to create admin account.

Role Types:

1 – Manager

2 – Accountant

3 - Sales and Marketing

![image](https://user-images.githubusercontent.com/46695666/121988830-0e4b2d00-cd69-11eb-8e46-3ec8e019d4f0.png)

### Home Page:

URL - http://127.0.0.1:5000/

Click on Create an Account to direct to signup page. If Username and Password already available select account type and hit sign in.

Sample ids:

Username: vish Password: 23 Account type: Employee (Role Assigned: Manager)

Username: sal Password: 15 Account type: Employee (Role Assigned: Accountant)

Username: mil Password: 01 Account type: Employee (Role Assigned: Sales and Marketing)

![image](https://user-images.githubusercontent.com/46695666/121989010-5ff3b780-cd69-11eb-8cca-c840edf4c12c.png)

### Admin Home Page:

- Employee would be able to see information of customers based on role assigned to him/her. 
- Managers can see personal information including SSN. Accountants can see account information and customer name. 
- Sales and Marketing reps can only see Customer Name and Contact information.

Select “Delete Expired data” to delete all the data that has been expired.

**Only managers can perform “Delete Expired data” action.**

Click on logout button to sign out

![image](https://user-images.githubusercontent.com/46695666/121989033-697d1f80-cd69-11eb-8382-cfef02b7b55d.png)
