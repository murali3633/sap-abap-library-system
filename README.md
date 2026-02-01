# SAP ABAP Library Management System

This project is a comprehensive Library Management System developed using SAP ABAP. It provides functionalities for managing books, student registrations, login authentication, and book transactions (issuing and returning).

## 📖 Project Overview 

The **Library Management System** is designed to streamline the operations of a library. It allows students to search for books, borrow them, return them, and manage their profiles. Administrators (or the system logic) can track book availability and manage user data.

## ✨ Key Features

*   **User Authentication**: secure login system for students/users.
*   **Registration**: Multi-step registration process for new users including personal details.
*   **Search Books**: Functionality to search for books by name or author.
*   **Issue Book (Get Book)**: Allows students to borrow books from the library.
*   **Return Book**: Logic to handle the return of borrowed books.
*   **Profile Management**: Students can view and update their personal information.
*   **Book History**: View history of borrowed books.

## 🛠️ Technical Specifications

### Main Program
*   **`ZA16_LIBRARY_MANAGEMENT`**: The main report that orchestrates the flow of the application, handling global data declarations and including sub-programs.

### Include Programs
The project is modularized using several include programs:
*   **`ZA16_LOGIN_PAGE`**: Handles the logic for the login screen (Screen 1000).
*   **`ZA16_HOME_PAGE`**: Manages the main menu/home screen (Screen 1001) navigation.
*   **`ZA16_REGISTRATION_PAGE`**: Controls the multi-step registration process (Screens 1002, 1003).
*   **`ZA16_SEARCH_BOOK`**: Logic for searching books in the database (Screen 1004).
*   **`ZA16_UPDATE_PROFILE`**: Allows users to update their details (Screen 1008).
*   **`ZA16_GET_BOOK` / `ZA16_RETURN_BOOK` / `ZA16_SHOW_BOOK`**: Modules handling specific book transaction logic.

### Database Tables (Custom)
The system relies on the following custom Z-tables:
*   **`ZA16_L_LOGIN`**: Stores user credentials (User ID, Password, Student ID).
*   **`ZA16_L_INFO`**: Stores detailed user information (Name, Roll No, Gender, Department, Address, etc.).
*   **`ZA16_L_BOOK_INFO`**: Inventory of books (Book ID, Name, Author, Price).
*   **`ZA16_L_GETBOOK`**: Records of book transactions (who borrowed what and when).

### Screens
*   **1000**: Login Page
*   **1001**: Home Page
*   **1002**: Registration Step 1
*   **1003**: Registration Step 2
*   **1004**: Search Book
*   **1005**: Get Book (Issue)
*   **1006**: Return Book
*   **1007**: Show Borrowed Books
*   **1008**: Update Profile

## 🚀 Installation & Setup

To use this project in your SAP environment:

1.  **Create Database Tables**: Create the custom tables (`ZA16_L_LOGIN`, `ZA16_L_BOOK_INFO`, `ZA16_L_GETBOOK`, `ZA16_L_INFO`) in SE11 with appropriate fields matching the data elements used in the code.
2.  **Create Main Program**: Create a new executable program named `ZA16_LIBRARY_MANAGEMENT` in SE38.
3.  **Create Includes**: Create the necessary include programs (`ZA16_LOGIN_PAGE`, etc.) and copy the respective code.
4.  **Create Screens**: Create screens (1000-1008) in SE51 for the main program. Design the layout using the Screen Painter to match the logic (fields, buttons) and assign the PBO/PAI modules.
5.  **Activate**: Activate all objects (Tables, Program, Includes, Screens).
6.  **Run**: Execute the main program `ZA16_LIBRARY_MANAGEMENT`.

## 📂 Project Structure

```
d:\LIBRARY-SYSTEM-SAP-ABAP-main
├── INCLUDE PROGRAMS/       # Source code for include programs
├── OUTPUT SCREENS/         # Screenshots of the application
├── SCREEN/                 # Screen flow logic files
├── TABLE/                  # Database table definitions (images/metadata)
├── ZA16_LIBRARY_MANAGEMENT.ABAP # Main program file
└── README.md               # Project documentation
```

