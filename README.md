# CLOUD-DATA-STORAGE-SERVER

### NAME: KOSAL AKSHAYA S
### REG NO: 212225020021

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
<img width="1920" height="930" alt="task 1 " src="https://github.com/user-attachments/assets/6c2773f6-4a58-4fbc-9d7c-7ad980487f37" />
<img width="1920" height="1032" alt="TASK 2" src="https://github.com/user-attachments/assets/e7d0c6f4-db2b-463d-9a30-ae844b5f7905" />
<img width="1920" height="871" alt="task 3" src="https://github.com/user-attachments/assets/016dfa9f-86da-429c-9c42-a9c0e44a04c5" />
<img width="1045" height="660" alt="Screenshot 2026-11-16 221338" src="https://github.com/user-attachments/assets/a54bf0b7-9caf-4459-95da-560a84b85c38" />
<img width="1033" height="513" alt="Screenshot 2026-11-16 221400" src="https://github.com/user-attachments/assets/2c035b73-664e-4865-ab75-f434a25b1225" />

## Result
Thus, an Amazon RDS database instance was successfully created and configured as a cloud data storage server. The database was securely connected to a web application, and data operations such as inserting, updating, and deleting records were successfully performed through the application.
