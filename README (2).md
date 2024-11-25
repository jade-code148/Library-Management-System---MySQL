# Library_Management_System

 This project streamlines library operations, enabling users to issue books, search titles, and access book details. It
 replaces manual record-keeping with an automated, user-friendly system for efficient management.

## Project Idea

The main objective of this project is to develop a comprehensive library management system that simplifies the management of books within a library. 

## Project Structure

    ├── LICENSE
    ├── README.md          <- README .
    ├── reports            <- Folder containing the final reports/results of this project.
    │   │
    │   └── query_report.pdf        <- Final query report in PDF for verifying data.
    │   
    ├── src                <- Source for this project.
        │
        ├── LMS_query.sql           <- Final query for this project.
        ├── LMS_schema.sql          <- Schema for this project.
        
--------

# Library Management System - Schema created

## Table: books

The `books` table stores information about books available in the library.

### Columns

| Column Name    | Data Type    | Constraints | Description                              |
|----------------|--------------|-------------|------------------------------------------|
| id             | SERIAL       | PRIMARY KEY | Unique identifier for the book            |
| title          | VARCHAR(255) | NOT NULL    | Title of the book                         |
| author         | VARCHAR(255) | NOT NULL    | Author of the book                        |
| category       | VARCHAR(255) | NOT NULL    | Category of the book                      |
| price          | DECIMAL(10,2)| NOT NULL    | Price of the book                         |
| status         | VARCHAR(255) | NOT NULL    | Status of the book (e.g., available, sold) |
| total_copies   | INT          | NOT NULL    | Total number of copies available           |

## Table: customers

The `customers` table stores information about the library customers.

### Columns

| Column Name    | Data Type    | Constraints | Description                              |
|----------------|--------------|-------------|------------------------------------------|
| id             | SERIAL       | PRIMARY KEY | Unique identifier for the customer        |
| first_name     | VARCHAR(255) | NOT NULL    | First name of the customer                |
| last_name      | VARCHAR(255) | NOT NULL    | Last name of the customer                 |
| email          | VARCHAR(255) | NOT NULL    | Email address of the customer             |
| phone_number   | VARCHAR(20)  | NOT NULL    | Phone number of the customer              |

## Table: issued_books

The `issued_books` table stores information about the books issued by customers.

### Columns

| Column Name    | Data Type    | Constraints       | Description                             |
|----------------|--------------|-------------------|-----------------------------------------|
| id             | SERIAL       | PRIMARY KEY       | Unique identifier for the issued book    |
| book_id        | INT          | NOT NULL          | Foreign key referencing books(id)        |
| customer_id    | INT          | NOT NULL          | Foreign key referencing customers(id)    |
| issue_date     | DATE         | NOT NULL          | Date when the book was issued            |
| due_date       | DATE         | NOT NULL          | Due date for returning the book          |
| return_date    | DATE         |                   | Date when the book was returned (optional)|
----



## Features

The Library Management System is designed with the following features in mind:

- User-friendly interface for easy navigation and interaction.
- Comprehensive entry for each book, containing details such as title, price, status, and quantity.
- Efficient search functionality to allow users to find books by their titles.
- Streamlined book issuing process to facilitate borrowing and returning.
- Centralized database to store and manage book information.
- Automated tracking of available books in the library.

By incorporating these features, the Library Management System aims to provide an efficient and user-friendly solution for managing library operations.

## Conclusion

The Library Management System is an automated solution that simplifies the management of books within a library. It offers a user-friendly interface, extensive book details, and efficient search functionality. By utilizing SQL queries, it interacts with a database to store and retrieve information effectively. With this system in place, the process of book management becomes more streamlined and convenient for both library staff and users.
The `books` table stores information about books available in the library.

