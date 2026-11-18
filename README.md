# CLOUD-DATA-STORAGE-SERVER

### NAME: DEVENDRAN G
### REG NO: 212225240030

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
<img width="767" height="718" alt="Screenshot 2026-11-18 082337" src="https://github.com/user-attachments/assets/4bbc0952-e782-47ba-bd12-40e9a992eab7" />
<img width="765" height="727" alt="Screenshot 2026-11-18 082605" src="https://github.com/user-attachments/assets/a68c3e0a-7b49-4f42-ac86-ce0821a4215b" />
<img width="762" height="718" alt="Screenshot 2026-11-18 084704" src="https://github.com/user-attachments/assets/f5586fe7-1be6-484e-bcd7-4a199b291fcc" />
<img width="756" height="762" alt="Screenshot 2026-11-18 085215" src="https://github.com/user-attachments/assets/bbe0a6b0-19c9-4177-8d4a-6cce1537425d" />
<img width="758" height="462" alt="Screenshot 2026-11-18 090654" src="https://github.com/user-attachments/assets/508de10b-e533-441d-8f04-f88389e53e43" />
<img width="762" height="461" alt="Screenshot 2026-11-18 090745" src="https://github.com/user-attachments/assets/d675a067-ce20-4e3c-aa8c-117c63bf301a" />
<img width="760" height="697" alt="Screenshot 2026-11-18 090758" src="https://github.com/user-attachments/assets/7f9ddd3f-76f2-4e93-ba3a-4e60916dd321" />
<img width="750" height="723" alt="Screenshot 2026-11-18 090924" src="https://github.com/user-attachments/assets/9ee09165-a1b4-46d2-a870-bfaa4b4f0dc6" />


## Result

Thus, an Amazon RDS database instance was successfully created and configured as a cloud data storage server. The database was securely connected to a web application, and data operations such as inserting, updating, and deleting records were successfully performed through the application.

