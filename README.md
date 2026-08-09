# LIBRARY MANAGEMENT SYSTEM
📌 Project Overview

The Library Management System is a console-based Python application designed to manage books in a library efficiently. It allows users to add, search, issue, return, and display books. The system uses Object-Oriented Programming (OOP) concepts and stores book records permanently using a CSV file.

🎯 Objectives
Manage library book records efficiently.
Add and search books.
Issue and return books.
Display available and issued books.
Store records using CSV file handling.
Demonstrate important Python OOP concepts.
✨ Features
➕ Add new books
🔍 Search books by Book ID
📖 Issue books
🔄 Return books
📋 Display all books
💾 Save records in CSV format
📂 Load records when the program starts
⚠️ Handle invalid input and file errors
🛠️ Technologies Used
Python 3
CSV File Handling
Object-Oriented Programming
Python Modules
from abc import ABC, abstractmethod
import csv
import os
🧩 OOP Concepts Used
1. Classes and Objects

The project uses multiple classes:

LibraryItem
Book
Member
Library
2. Encapsulation

Private attributes are used to protect the data of objects.

self.__book_id
self.__title
self.__author
self.__status

Getter and setter methods are used to access and modify these attributes.

3. Inheritance

The Book class inherits from the abstract LibraryItem class.

class Book(LibraryItem):
4. Abstraction

LibraryItem is an abstract base class implemented using Python's abc module.

class LibraryItem(ABC):

    @abstractmethod
    def display(self):
        pass
5. File Handling

The system uses records.csv to store book information.

The program can:

Read existing records.
Write new records.
Update book status.
Save changes automatically.
6. Exception Handling

The system handles invalid user input using try-except.

try:
    choice = int(input("Enter your choice: "))
except ValueError:
    print("Invalid input! Please enter numbers only.")
📁 Project Structure
LibraryManagementSystem/
│
├── main.py
├── records.csv
├── README.md
│
└── screenshots/
    ├── add_book.png
    ├── search_book.png
    ├── issue_book.png
    ├── return_book.png
    └── display_books.png
📄 CSV Data File

The project uses records.csv to store book records.

Example:

Book ID,Title,Author,Status
101,Python Basics,John Smith,Available
102,Data Structures,James Lee,Issued
103,Machine Learning,Andrew Ng,Available
▶️ How to Run the Project
Step 1: Install Python

Install Python 3.x on your computer.

Step 2: Open the Project

Open the project folder in VS Code, PyCharm, or another Python IDE.

Step 3: Run the Program

Open the terminal and execute:

python main.py
Step 4: Use the Menu

The program will display:

===== LIBRARY MANAGEMENT SYSTEM =====
1. Add Book
2. Search Book
3. Issue Book
4. Return Book
5. Display Books
6. Exit

Enter your choice:
💻 Sample Output
Add Book
Enter your choice: 1
Enter Book ID: 104
Enter Title: Computer Networks
Enter Author: Tanenbaum

Book added successfully!
Search Book
Enter your choice: 2
Enter Book ID to search: 101

Book Found:
ID: 101 | Title: Python Basics | Author: John Smith | Status: Available
Issue Book
Enter your choice: 3
Enter Book ID to issue: 101

Book issued successfully!
Return Book
Enter your choice: 4
Enter Book ID to return: 101

Book returned successfully!
Display Books
Enter your choice: 5

------ Available Books ------
ID: 101 | Title: Python Basics | Author: John Smith | Status: Available
ID: 102 | Title: Data Structures | Author: James Lee | Status: Issued
ID: 103 | Title: Machine Learning | Author: Andrew Ng | Status: Available
📋 Project Requirements
Requirement	Status
Classes & Objects	✅ Implemented
At least 3 Classes	✅ Implemented
Encapsulation	✅ Implemented
Getters & Setters	✅ Implemented
Inheritance	✅ Implemented
Abstraction	✅ Implemented
abc Module	✅ Implemented
File Handling	✅ Implemented
CSV File	✅ Implemented
Exception Handling	✅ Implemented
Add Book	✅ Implemented
Search Book	✅ Implemented
Issue Book	✅ Implemented
Return Book	✅ Implemented
Display Books	✅ Implemented

