# Exam Management System

## Overview

The Exam Management System is a software application designed for exam conducting associations to manage exam-related activities. This system allows users to perform operations such as adding, modifying, and deleting exams, as well as registering and removing students from exams. Additionally, it provides functionality to display exam and student details, and generate various reports.

## Features

1. Add an exam
2. Modify an exam
3. Delete an exam
4. Display all exam details
5. Register a student
6. Delete a student
7. List the students registered for an exam
8. List the number of students for each exam
9. List the exams registered by a student
10. Display all details

## Technologies Used

- **Programming Language:** Python 3.8.5
- **Database Management System:** MySQL 8.0.21
- **Python MySQL Connector:** To facilitate connectivity between Python and MySQL.

## Database Design

### Database: `edms`

#### Table: `Exam`
- `Examno` INT PRIMARY KEY
- `Examname` VARCHAR(30) UNIQUE
- `Examday` INT NOT NULL
- `Exammonth` INT NOT NULL
- `Examyear` INT NOT NULL
- `Class` INT NOT NULL
- `Fee` INT NOT NULL

#### Table: `Student`
- `STID` INT PRIMARY KEY
- `Firstname` VARCHAR(30)
- `Lastname` VARCHAR(30) NOT NULL
- `Mobilenumber` BIGINT NOT NULL
- `Emailid` VARCHAR(30) NOT NULL
- `Schoolname` VARCHAR(50)

## Hardware Requirements

- **Processor:** Intel® Core™ i3 CPU
- **CPU Speed:** 2.67 GHz
- **RAM:** 4 GB
- **Hard Disk Memory:** 80 GB
- **Cache:** 512 KB
- **Monitor**
- **Keyboard**

## Software Requirements

- **Operating System:** Microsoft Windows 10
- **Software:** 
  - Python 3.8.5
  - MySQL Server 8.0.21

## Installation and Setup

1. **Install Python 3.8.5**: Download and install Python from [python.org](https://www.python.org/downloads/).

2. **Install MySQL Server 8.0.21**: Download and install MySQL from [mysql.com](https://dev.mysql.com/downloads/mysql/).

3. **Set up the Database**:
   - Create a database named `edms` in MySQL.
   - Execute the following SQL commands to create the required tables:

     ```sql
     CREATE TABLE Exam (
         Examno INT PRIMARY KEY,
         Examname VARCHAR(30) UNIQUE,
         Examday INT NOT NULL,
         Exammonth INT NOT NULL,
         Examyear INT NOT NULL,
         Class INT NOT NULL,
         Fee INT NOT NULL
     );

     CREATE TABLE Student (
         STID INT PRIMARY KEY,
         Firstname VARCHAR(30),
         Lastname VARCHAR(30) NOT NULL,
         Mobilenumber BIGINT NOT NULL,
         Emailid VARCHAR(30) NOT NULL,
         Schoolname VARCHAR(50)
     );
     ```

4. **Install Python Packages**:
   - Use pip to install the required Python packages:
     ```bash
     pip install mysql-connector-python
     ```

5. **Configure Database Connection**:
   - Update the database connection settings in your Python code to match your MySQL server credentials.

## Usage

1. **Run the Application**: Execute the Python script to start the application.

2. **Perform Operations**:
   - Use the provided options to add, modify, or delete exams and students.
   - Generate reports and view details as needed.

## Contributing

Contributions to this project are welcome. Please fork the repository and submit a pull request with your proposed changes.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Contact

For any questions or issues, please contact [praveenben703@gmail.com](praveenben703@gmail.com).

