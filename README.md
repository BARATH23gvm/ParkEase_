🚗 Car Parking Management System
This is a GUI-based Java application designed to handle parking management functions such as vehicle entry, slot allocation, release, and data monitoring using a MySQL database for backend storage.

📁 Project Structure
CarParking.java – Main interface for parking a vehicle.

CarRele.java – Interface for releasing a parked vehicle and updating end time.

parkingdata.java – Displays all parking data stored in the database.

carpark.java – Class model representing a parked vehicle's data.

🛠️ Technologies Used
Java Swing for GUI

JDBC for MySQL database interaction

MySQL for data storage

⚙️ Setup Instructions
Install MySQL and create a database called parking.

Run the following SQL to create the table:

sql
Copy
Edit
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
Update Database Credentials
In all Java files (CarParking.java, CarRele.java, and parkingdata.java), replace:

java
Copy
Edit
String uname = "root";
String pass = "barath23102003";
with your own MySQL username and password.

Compile and Run the Application

Use any IDE (like Eclipse or IntelliJ) or command line to compile and run:

bash
Copy
Edit
javac *.java
java CarParking
🚦 How It Works
Car Entry (CarParking.java)

Select a parking slot.

Enter car number, name, mobile number, and timing details.

Save entry which stores it in the database and carpark.txt.

Car Release (CarRele.java)

Enter the same car number and name.

Enter end time and release the vehicle.

Cost is calculated and updated.

View Data (parkingdata.java)

Shows all parked and released vehicle information including cost.

📌 Notes
Duration is calculated in hours, and cost is 5 INR/hour or 100 INR/day.

Text file carpark.txt is also used to keep a local record.

GUI includes checkbox-based parking slot selection.
