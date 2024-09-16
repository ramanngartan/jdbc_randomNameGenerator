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
git clone https://github.com/your-repository/jdbc-cmd-professor-skeleton.git
cd jdbc-cmd-professor-skeleton

3. Set Up the MySQL Database
Open MySQL Workbench or any other MySQL client.
Run the following SQL script to create the necessary tables:
sql
SOURCE path/to/lab01-databank.sql;

4. Build the Project
Use Maven to build the project and download dependencies.


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

📝 License
This project is licensed under the MIT License - see the LICENSE file for details.
