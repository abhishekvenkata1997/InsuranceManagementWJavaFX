# InsuranceManagementJava

>>Requirements:

To install NetBeans with Java 18, follow these steps
Download the NetBeans installer from the official website (https://netbeans.org/downloads/).
Install Java 18 by following the instructions on the official website (https://www.oracle.com/java/technologies/javase-jdk18-downloads.html). Make sure to choose the correct version for your operating system.
Once Java 18 is installed, run the NetBeans installer and follow the on-screen instructions to complete the installation.
To confirm that NetBeans is installed and working properly, open the application and create a new project. In the New Project window, select the Java category and choose the Java Application project type. Click Next and enter a project name and location, then click Finish.
NetBeans should now create a new project and open it in the editor. You can test that Java 18 is working properly by adding the following code to the main method in the Main.java file: System. out.println("Hello, World!");
Now download the program hellofx, a coffee mug icon shows to the right of the project. This suggests the project has been downloaded in the right format. Click the Run button in the toolbar or press F6 to run the program
However for the backend to work, you will have to download Mysql and build a database:

>>MYSQL
To download MySQL and build a database, follow these steps:
1. Download and install MySQL from the official website (https://www.mysql.com/downloads/). Make sure to choose the correct version for your operating system and follow the on-screen instructions to complete the installation.
2. Once MySQL is installed, open the MySQL command line interface by entering the "MySQL" command in a terminal or command prompt window.
3. In the MySQL command line interface, create a new database by entering the following command

>>Code:

CREATE database ood_project; 
USE ood_project;
CREATE TABLE user_registration (
id BIGINT PRIMARY KEY AUTO_INCREMENT, full_name varchar(250) NOT NULL,
email_id varchar(250) NOT NULL,
password varchar(250)
     );

CREATE TABLE insurance_plan (
id BIGINT PRIMARY KEY AUTO_INCREMENT, email_id varchar(250) not null, insurance_type varchar(250) not null,
insurance_name varchar(250) not null, monthly_premium int(11) not null, tenure int not null
);

>>In the jdbcDAO.java file please remove instances of

Connection connection = DriverManager.getConnection("jdbc:mysql://localhost:3306/ood_project?allowPublicKeyRetrieval=true& useSSL=false","root","Abhi$0454"); and add your own MySQL Db
