# C++ Personal Finance Tracker

A simple **C++17 console application** for recording income and expenses, checking your balance, and reviewing monthly spending. This project was built for learning and practicing core C++ concepts.

![Language](https://img.shields.io/badge/language-C%2B%2B17-blue)
![Platform](https://img.shields.io/badge/platform-Windows-lightgrey)

## Features

- Add income and expense transactions in PKR
- Save each transaction's amount, category, description, and date
- View saved transactions and an overall financial summary
- Generate reports for a selected month
- Filter transactions by category (case-insensitive)
- Validate user input and reload saved records on the next run
- Uses the C++ standard library only — no third-party packages

## Requirements

- Windows 10/11
- A C++17 compiler, such as g++ (MinGW-w64) or MSVC

## Build and run

### Using g++ on Windows

1. Install a C++ compiler that includes `g++`.
2. Download this repository and open Command Prompt or a terminal in the project folder.
3. Compile the program:

   ```bat
   g++ -std=c++17 -Wall -Wextra -pedantic main.cpp -o finance_tracker.exe
   ```

4. Run it:

   ```bat
   finance_tracker.exe
   ```

If `g++` is not recognized, install/configure MinGW-w64, add its `bin` directory to your `PATH`, and reopen the terminal.

### Using Visual Studio

Install Visual Studio with the **Desktop development with C++** workload. Open or create a C++ console project, use this repository's `main.cpp`, then build and run with **Ctrl+F5**.

## Main menu

1. Add income
2. Add expense
3. View all transactions
4. View financial summary
5. View monthly report
6. Filter transactions by category
7. Exit

## Example report

For a month with PKR 85,000 income and PKR 1,200 expenses, the report would look like this:

```text
Report for 2026-10
Income:       PKR 85000.00
Expenses:     PKR 1200.00
Monthly net:  PKR 83800.00
Transactions: 2
```

Enter a month in `YYYY-MM` format (for example, `2026-10`) to view that month's report.

## Data storage and privacy

Transactions are stored locally in `transactions.txt` in the program's current working directory. Back up this file if you want to keep your records. **Do not commit real personal financial records to GitHub.**

Each line uses this format:

```text
Type|Amount|Category|Description|Date
```

The `|` character separates fields, so avoid using it in categories or descriptions. Date validation checks the format and basic month/day ranges, but does not verify every calendar date.

## C++ concepts practiced

- Structures, vectors, functions, loops, and `switch`
- Input validation and exception handling
- File input/output
- String processing and case-insensitive matching
- Calculating totals and formatting console output

## Ideas for future improvements

- Edit or delete transactions
- Search by date range
- Export reports to CSV
- Add unit tests or a graphical interface

## Disclaimer

This is a learning project, not accounting or financial advice. Always keep a backup of your local data file.
