# CLOUD-DATA-STORAGE-SERVER

### NAME: MUDDA DIVYANKA SHRUTHI
### REG NO: 212225020028

## Aim

To create and configure an Amazon Relational Database Service (Amazon RDS) instance as a cloud data storage server, configure the required security settings, connect it to a web application, and perform database operations using the application.

## Algorithm / Steps

1. Create a Security Group for the RDS database.
2. Add an inbound rule to allow MySQL (Port 3306) access from the Web Security Group.
3. Create a DB Subnet Group using two Availability Zones.
4. Launch an Amazon RDS MySQL database instance.
5. Configure the database with the required identifier, username, password, storage, and instance class.
6. Associate the database with the created Security Group and Subnet Group.
7. Wait until the database status becomes **Available**.
8. Copy the RDS endpoint.
9. Open the web application using the provided Web Server IP address.
10. Enter the RDS endpoint, database name, username, and password.
11. Connect the application to the database.
12. Verify the connection by adding, editing, and deleting records in the Address Book application.


## Program

### Security Group Configuration

* Security Group Name: **DB Security Group**
* Inbound Rule: **MySQL/Aurora (3306)**
* Source: **Web Security Group**

### DB Subnet Group

* Name: **DB-Subnet-Group**
* VPC: **Lab VPC**

### Amazon RDS Configuration

* Engine: **MySQL**
* Template: **Dev/Test**
* Availability: **Multi-AZ**
* DB Instance Identifier: **lab-db**
* Username: **main**
* Password: **lab-password**
* Instance Class: **db.t3.micro**
* Storage: **20 GB (General Purpose SSD)**

### Connect the Application

```text
Endpoint : <RDS Endpoint>
Database : lab
Username : main
Password : lab-password
```

After submitting the above details, perform Add, Edit, and Delete operations on the Address Book application.

## Output
<img width="1535" height="728" alt="Screenshot 2026-11-16 102153" src="https://github.com/user-attachments/assets/4e6b7811-86ec-4c04-a595-4816b175c8e1" />
<img width="1535" height="722" alt="Screenshot 2026-11-16 102337" src="https://github.com/user-attachments/assets/7efc6e60-ea51-40a0-b095-12bdee48b1a3" />
<img width="997" height="678" alt="Screenshot 2026-11-16 102917" src="https://github.com/user-attachments/assets/b7bcff49-6cf3-450d-85ca-371fbfaf372f" />
<img width="1006" height="658" alt="Screenshot 2026-11-16 102939" src="https://github.com/user-attachments/assets/49390a46-b05e-4800-bd9e-6a34bffe3365" />
<img width="1006" height="702" alt="Screenshot 2026-11-16 103951" src="https://github.com/user-attachments/assets/14579672-df6e-400a-8af5-45e83c80c885" />
<img width="1080" height="693" alt="WhatsApp Image 2026-11-16 at 20 19 20" src="https://github.com/user-attachments/assets/e3122ed3-9cf6-424b-9121-481f09c33b98" />
<img width="1532" height="728" alt="Screenshot 2026-11-16 142931" src="https://github.com/user-attachments/assets/5c67b377-e402-44c8-a9b8-ab3505831116" />

## Result

Thus, an Amazon RDS database instance was successfully created and configured as a cloud data storage server. The database was securely connected to a web application, and data operations such as inserting, updating, and deleting records were successfully performed through the application.
