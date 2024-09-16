JDBC-CMD Professor Skeleton

A simple Java Command-Line JDBC application that connects to a MySQL database, generating random professor records. This project demonstrates JDBC database manipulation and uses the Picocli library for command-line interface parsing. Random professor data is generated using the PODAM library.

Features
🔄 Random Professor Generation: Generate random professor records and insert them into a MySQL database.
⚙️ Customizable: Define the number of records to generate via command-line arguments.
🗄️ Database Truncation: Truncate existing records before inserting new data.
📋 Logs: Provides informative logging using SLF4J and Logback.
🛠️ Requirements
Java 17
MySQL 8.x or higher
Maven 3.x or higher
MySQL Workbench (Optional)
🚀 Getting Started
1. Clone the Repository
bash
Copy code
git clone https://github.com/your-repository/jdbc-cmd-professor-skeleton.git
cd jdbc-cmd-professor-skeleton
2. Set Up the MySQL Database
Open MySQL Workbench or any other MySQL client.
Run the following SQL script to create the necessary tables:
sql
Copy code
SOURCE path/to/lab01-databank.sql;
3. Build the Project
Use Maven to build the project and download dependencies.

bash
Copy code
mvn clean install
🏃‍♂️ Running the Application
To run the application, execute the following command:

bash
Copy code
java -jar target/JDBC-CMD-Professor-Skeleton-1.jar -u <username> -p <password> -url <jdbc-url> -g <count>
<username>: Your MySQL username.
<password>: Your MySQL password.
<jdbc-url>: JDBC URL to your MySQL instance. Example: jdbc:mysql://localhost:3306/databank?useSSL=false&allowPublicKeyRetrieval=true&serverTimezone=UTC
<count>: Number of random professor records to generate.
Example:
bash
Copy code
java -jar target/JDBC-CMD-Professor-Skeleton-1.jar -u cst8277 -p 8277 -url jdbc:mysql://localhost:3306/databank?useSSL=false&allowPublicKeyRetrieval=true&serverTimezone=UTC -g 5
🗄️ Verifying Database Records
After running the application, check if records have been inserted into the PROFESSOR table:

sql
Copy code
SELECT * FROM PROFESSOR;
🛠️ Project Structure
css
Copy code
JDBC-CMD-Professor-Skeleton/
├── src/
│   └── main/
│       ├── java/
│       └── resources/
│           ├── firstnamePool.txt
│           ├── lastnamePool.txt
│           ├── degreePool.txt
│           └── majorPool.txt
├── pom.xml
└── README.md
src/main/java/: Contains the main Java source code.
src/main/resources/: Contains resource files used for random data generation.
pom.xml: Maven configuration file.
📚 Libraries and Tools
JDBC - For database interaction.
PODAM - For generating random professor data.
Picocli - For command-line argument parsing.
SLF4J and Logback - For logging.
⚠️ Troubleshooting
Common Issues:
Multiple SLF4J Bindings Warning: If you see a warning about multiple SLF4J bindings, Logback is being used as the primary logger. This warning can be ignored unless there are specific errors.
Database Connection Issues: Double-check your JDBC URL, MySQL username, and password.
Maven Dependency Issues: Run the following to update Maven dependencies:
bash
Copy code
mvn clean install -U
📝 License
This project is licensed under the MIT License - see the LICENSE file for details.
