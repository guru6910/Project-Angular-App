# $${\color{red} \textbf{Project}: \textbf{Angular} \ \textbf{App}}$$

#### ${\color{red} \textbf{Frontend :}}$  ${\color{yellow} \textbf{Angular,Nodejs}}$
#### ${\color{red} \textbf{Backend :}}$  ${\color{yellow} \textbf{Java-Springboot}}$
#### ${\color{red} \textbf{Database :}}$  ${\color{yellow} \textbf{Mariadb}}$


**Create a Security Group with the port of 80,22,3306 and 8080**

**Create Three Instance**

1. Frontend-Server
2. Backend-Server
3. Database-Server
   
![image](https://github.com/guru6910/Project-Angular-App/assets/169146749/f8d1ab54-37c3-4874-b95e-bd48aae68905)


### ${\color{green} \textbf{Create RDS}}$
standard create

Mariadb

Free tier

Username & Password

Connect to EC2 instance

Security group select 

![image](https://github.com/guru6910/Project-Angular-App/assets/169146749/f6c1561b-6d2d-45a0-beed-223e6a5cedcb)



## ${\color{red} \textbf{Set up Database Server}}$

1. install mariadb and start mariadb.
````
yum install mariadb105-server -y
systemctl start mariadb.service
````
2. install git and clone the Project Repo.
````
yum install git -y
git clone https://github.com/guru6910/Project-Angular-App
````
### ${\color{yellow} \textbf{Log in Database}}$

````
mysql -h <endpoint> -u admin -ppasswd123
````
````
create database springbackend;
````
````
exit
````
````
cd Project-Angular-App/database
````
````
mysql -h <endpoint> -u admin -ppasswd123 springbackend < springbackend.sql
````
````
mysql -h <endpoint> -u admin -ppasswd123
````
````
use springbackend;
````
````
describe springbackend;
````
````
exit
````

## ${\color{red} \textbf{Set up Backend Server}}$

1. Install java 
````
yum install java -y
````
2. Install Maven 
````
yum install maven -y
````
3. install git and clone Project Repo
````
yum install git -y
git clone https://github.com/guru6910/Project-Angular-App
````
4. Create Database Connection with backend
````
cd Project-Angular-App/spring-backend
````
````
vim src/main/resources/application.properties
````
### ${\color{green} \textbf{NOTE : }}$ Add endpoint of database, Username and Password.


5. Build the project using Maven
````
mvn clean package-Dmaven.test.skip=true
````
6. Run the application:
````
java -jar target/spring-backend-v1.jar
````

## ${\color{red} \textbf{Set up Frontend Server}}$

1. install git and clone
````
yum install git -y
git clone https://github.com/guru6910/Project-Angular-App
````
2. enter the angular-frontend
````
cd Project-Angular-App/angular-frontend/
````
3. install nodejs and npm
````
yum install nodejs npm
````
4. Check Node.js and npm versions
````
node -v
npm -v
````
5. Install Angular CLI globally
````
sudo npm install -g @angular/cli@14.2.1
````
6. Verify Angular CLI installation
````
ng version
````
7. Connect with Backend Server  
````
cd src/app/services
sudo nano worker.service.ts
````
### ${\color{green} \textbf{NOTE : }}$ Add public ip of Backend server.

8. Install project dependencies.
````
npm install
ng build 
sudo ng serve --host 0.0.0.0 --port=80
````
