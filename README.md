# 🚗 Car Parking Management System

This is a GUI-based Java application designed to manage car parking, including booking slots, releasing vehicles, and viewing all parking data. The system uses a MySQL database to store vehicle information.

---

## 📁 Project Files

- `CarParking.java` – GUI for parking a car.
- `CarRele.java` – GUI for releasing a parked car.
- `parkingdata.java` – View all current parking data.
- `carpark.java` – Model class representing a parking record.

---

## 🛠️ Technologies Used

- Java (Swing for GUI)
- JDBC for MySQL connectivity
- MySQL for data storage

---

## ⚙️ Setup Instructions

### 1. MySQL Setup

Create a database named `parking`, then run:

'''sql
CREATE TABLE parkingdata1 (
  carnum VARCHAR(20),
  name VARCHAR(100),
  cellno VARCHAR(20),
  placeno VARCHAR(10),
  startTime VARCHAR(10),
  duration INT,
  cost INT,
  endTime VARCHAR(20)
);

### 2. Update Credentials
In your Java files, make sure to update the database credentials in this section:

java
Copy
Edit
String url = "jdbc:mysql://localhost:3306/parking";
String uname = "root"; // your MySQL username
String pass = "barath23102003"; // your MySQL password
Replace uname and pass with your actual MySQL login.

### 3. Compile and Run
You can compile and run the program using the terminal or your preferred IDE.

bash
Copy
Edit
javac *.java
java CarParking
🚦 How It Works
CarParking.java:
Book a parking slot by entering vehicle and owner details. Slot is saved in MySQL and appended to a text file carpark.txt.

CarRele.java:
Release a vehicle by entering car number and name. Updates endTime and calculates total cost.

parkingdata.java:
View a full log of all parked and released vehicles, including duration and cost.

💰 Pricing Logic
₹5 per hour or ₹100 per day.

Cost is calculated based on the entered duration at the time of parking.

📌 Notes
GUI components are built using Swing.

Parking slots are selected using checkbox groups (A1–F12).

Local logs are written to carpark.txt.

