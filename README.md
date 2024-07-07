# $${\color{red} \textbf{Project}: \textbf{Angular} \ \textbf{App}}$$
**Create a Security Group with the port of 80,22,3306 and 8080**

**Create Three Instance**

1. Frontend-Server
2. Backend-Server
3. Database-Server

### ${\color{green} \textbf{Create RDS}}$



## ${\color{red} \textbf{Set up Database Server}}$

````
yum install mariadb105-server -y
systemctl start mariadb.service
````
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

````
yum install java -y
````
````
yum install maven -y
````
````
yum install git -y
git clone https://github.com/guru6910/Project-Angular-App
````
````
cd Project-Angular-App/spring-backend
````
````
vim src/main/resources/application.properties
````
### ${\color{red} \textbf{NOTE : }}$ Add endpoint of database, Username and Password.

