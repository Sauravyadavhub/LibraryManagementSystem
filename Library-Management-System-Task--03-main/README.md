# Library-Management-System-Task--03
CodSoft
# Library Management System (C++)
This C++ program implements a basic Library Management System that allows users to manage a collection of books. The features include displaying all books, extracting book details by ID, and adding new books to the system.

## Code Walkthrough:
Headers and Namespace

## #include<iostream>: For input/output operations.
## #include<fstream>: For file handling to store and retrieve book details.
## using namespace std: To avoid prefixing std:: before standard library functions.
Class Definition

## Class Name: temp
Private Members:
string id, name, author, search: Store book details and search query.
fstream file: For file operations.
Public Methods:
addBook(): Adds a new book to the system.
showAll(): Displays all books stored in the system.
extractBook(): Searches for a specific book by ID and displays its details.
Main Function

## Displays a menu with options:
Show all books.
Extract book by ID.
Add new books (Admin functionality).
Exit the program.
Takes user input to perform the chosen action and calls the corresponding class method.
Class Methods

## addBook()
Prompts the user to enter book details (ID, name, author).
Appends the details to a file (bookData.txt) in the format: id*name*author.
showAll()

Opens bookData.txt in read mode.
Reads and displays all book entries in a tabular format with columns for ID, name, and author.
Iterates through the file using getline() until the end of the file.
extractBook()

Calls showAll() to display all books for reference.
Prompts the user to enter the book ID to extract.
Searches the file for a matching ID and displays the book details if found.
Displays a success message upon finding the book.
File Handling

The program uses the fstream class to perform:
ios::out | ios::app: Open file in append mode for adding new books.
ios::in: Open file in read mode to display or extract book details.
Each book entry is stored in the file in the format: id*name*author.
Execution Flow

The user selects an option from the menu.
Based on the choice:
Calls showAll() to list all books.
Calls extractBook() to search and display a specific book.
Calls addBook() to add a new book to the system.
The program exits when the user chooses option 4.
Sample Input/Output

# Menu Display:

mathematica
Copy code
----------------------------------
1-Show All Books
2-Extract Book
3-Add books(ADMIN)
4-Exit
----------------------------------
Enter Your Choice ::
Add Book Example:

mathematica
# Copy code
Enter Book ID :: 101
Enter Book Name :: C++ Programming
Enter Book's Author name :: Bjarne Stroustrup
Show All Books Example:

## markdown
Copy code
    Book Id             Book Name               Author's Name
    101                 C++ Programming         Bjarne Stroustrup
Extract Book Example:

## mathematica
Copy code
Enter Book Id :: 101

    Book Id             Book Name               Author's Name
    101                 C++ Programming         Bjarne Stroustrup

# Book Extracted Successfully...!
## Files Used:
bookData.txt: Stores the book details in the format: id*name*author. 

# Future Improvements:
## Add input validation to handle invalid inputs or file errors.
## Improve the UI/UX by creating a more interactive interface.
## Allow updating or deleting book records.


This program provides a simple implementation of a library management system. Contributions and enhancements are welcome!





