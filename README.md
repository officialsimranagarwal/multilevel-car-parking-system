# Multilevel Car Parking System 🚗

![C++](https://img.shields.io/badge/c++-%2300599C.svg?style=for-the-badge&logo=c%2B%2B&logoColor=white)
![Persistence](https://img.shields.io/badge/Data-Binary_File_I%2FO-blue?style=for-the-badge)
![OOP](https://img.shields.io/badge/Design-OOP-green?style=for-the-badge)

## 📖 Overview

A comprehensive **C++ Console Application** designed to manage a multi-level parking facility. It demonstrates Object-Oriented Programming (OOP) principles and persistent data storage using binary file handling.

## 🏗️ Class Architecture

### `class car`
The core entity representing a parking record.
-   **Attributes**:
    -   `vno` (int): Vehicle license number.
    -   `count` (float): Duration of stay (hours).
    -   `dname` (char[]): Driver's name.
    -   `l` (char[]): Parking slot identifier.
-   **Methods**:
    -   `input()`: Captures driver details and validates parking slot availability.
    -   `cal()`: Calculates billing based on generic vs. VIP rates.
    -   `output()`: Displays the receipt details.

## 💾 Data Persistence (File Handling)

The system avoids data loss using C++ File Streams (`<fstream>`):
-   **Storage**: Records are stored in `parking3.dat`.
-   **Mechanism**:
    -   `ifstream`: Reads existing records in binary mode (`ios::binary | ios::in`).
    -   `ofstream`: Appends new parking entries (`ios::binary | ios::app`).
-   **Deletion Logic**:
    -   Creates a temporary file `temp.dat`.
    -   Copies all records *except* the one being deleted.
    -   Removes the old file and renames the temp file.

## 🔐 Security Features

-   **Login System**: A basic authentication mechanism checks against a hardcoded "admin" password (`pass`) using character masking (`*`) for security during input.

## 🚀 Usage

1.  Compile:
    ```bash
    g++ main.cpp -o parking_system
    ```
2.  Run:
    ```bash
    ./parking_system
    ```

## 🤝 Contributing

Contributions are welcome! Please see [CONTRIBUTING.md](CONTRIBUTING.md) for details.

## 👤 Author

**Simran Agarwal**
-   [Profile](https://github.com/officialsimranagarwal)
-   [LinkedIn](https://linkedin.com/in/simran-agarwal-54751b191)

---
*Generated with ❤️ by Simran Agarwal*
