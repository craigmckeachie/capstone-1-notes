# Capstone 1: Accounting Ledger Notes

## Progress

- [Share Your Repository Here](https://docs.google.com/spreadsheets/d/13WrWNzOfjs91UOan0ee9owZ6cHfo6bcuIGqDGO6Rw3Q/edit?gid=1229912940#gid=1229912940)

## Support

- [Sign up for support at the Help Desk](https://docs.google.com/spreadsheets/d/1UWuNC9R2MhbqtK6G_SofujeGhokevH7buV8egLxrNPE/edit?gid=998355056#gid=998355056)

## Data

Here is [how I generated the transactions.csv file](https://gemini.google.com/share/5b2e23e0bfea).

Here is the file you should use for the Capstone: [transactions.csv](./transactions.csv)

## Project Name

Here are some [ideas for project names](https://gemini.google.com/share/f73463b545a8). Be sure to use kebab-case.

## Classes

- `Application`, `Program`, `App`, `AccountingApp` will be the UI and have your `main` method all the other UI methods will be static and you will need a shared static `Scanner` field

## Terminology

- Deposit and Payment are each a `Transaction`

* **Payments (Expenses) are Negative:** These represent money leaving your account. For example, buying a coffee or paying a bill is recorded as **-25.00**.
* **Deposits (Income) are Positive:** These represent money entering your account. For example, receiving your salary or a refund is recorded as **1500.00**.

---

### How to Think About It

If you were to sum up the entire `amount` column in your CSV, the math works naturally:

$$Total Balance = \sum (Deposits) + \sum (Payments)$$

Since payments are negative numbers, adding them effectively subtracts them from your total.

### Common Exceptions

While the "Negative = Expense" rule is standard for **Transaction History**, you might see it differently in other contexts:

- **Accounting (Debits/Credits):** In formal double-entry bookkeeping, the terms "Debit" and "Credit" are used instead of positive and negative, and their "direction" depends on whether the account is an Asset, Liability, or Equity.
- **Budgeting Apps:** Some apps display expenses as positive numbers just for visual clarity (e.g., "You spent $50 today"), but in the underlying database or CSV export, they are almost always stored as negative values to keep the math accurate.

## Features

Pattern: each screen is a method and should start with a verb `runHomeScreen`, `runAddDepositScreen`

> `promptFor` isn't ideal because most screens do more than prompt they prompt and read and display menu
> `displayMenu` isn't ideal because most screens display a menu and then do something else like prompt the user to choose and then show another screen

- HomeScreen
  - AddDepositScreen
  - MakePaymentScreen
  - LedgerScreen
    - DisplayAllEntriesScreen
    - DepositsScreen
    - PaymentsScreen
    - ReportsScreen
      - MonthToDateScreen
      - PreviousMonthScreen
      - YearToDateScreen
      - PreviousYearScreen
      - SearchByVendorScreen
      - CustomSearchScreen (bonus search by all the listed fields at once but they are all optional)
      - goBackToLedger
    - goBackToHome
  - Exit

Examples to reference:
[Date Examples here](https://github.com/craigmckeachie/wb3-examples/blob/254e8a8e90eda003381a9f9a331b2cc704f8ddf5/src/main/java/com/pluralsight/LocalDateTimeFormatterExample.java)

# Screens (with Menus)

Use these as reference examples:

- [Screen Example Diagram](https://github.com/craigmckeachie/wb3-examples/blob/main/src/main/java/com/pluralsight/ScreenExampleDiagram.txt)
- [Screen Example Code](https://github.com/craigmckeachie/wb3-examples/blob/main/src/main/java/com/pluralsight/ScreenExample.java)
- [Library App Diagram](https://github.com/craigmckeachie/wb3-examples/blob/main/src/main/java/com/pluralsight/LibraryAppDiagram.txt)
- [Library App](https://github.com/craigmckeachie/wb3-examples/blob/main/src/main/java/com/pluralsight/LibraryApp.java)
- [Screen Feature Naming](https://github.com/craigmckeachie/wb3-examples/blob/main/src/main/java/com/pluralsight/FeatureScreenNaming.md)

> Note: this example only has two levels of menus and you have three levels in the Capstone.

## Read File into Object

- [Example of Reading a File](https://github.com/craigmckeachie/wb3-examples/blob/main/src/main/java/com/pluralsight/FileReaderExample.java)
- [Reading a csv File into Objects](https://github.com/craigmckeachie/payroll-calculator/blob/main/src/main/java/com/pluralsight/App.java)
  - [Explanation of the Reading a csv File into Objects code](https://gemini.google.com/share/13e8571c59be)

## Write to File

- [Simple Example of Writing to a File](https://github.com/craigmckeachie/wb3-examples/blob/main/src/main/java/com/pluralsight/FileWriterExample.java)

<!-- ## Example

- [Pawsitive Playlist](https://www.youtube.com/playlist?list=PLovJOX3wAkpsqtVEbPtJSMhzfevMwN5Z6)
- [Pawsitive Code](https://github.com/craigmckeachie/workbook-3/tree/main/Pawsitive)
  - click on branch drop down to see code at different points -->
