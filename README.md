# Robotic Process Automation

This repository contains automation workflows created using UiPath. Below is a description of the projects and their functionality.

## 2LD_SaldainiuAutomatas

This project simulates a candy vending machine process. The workflow includes:
- Asking the user for the type of candy they want to purchase.
- Asking for the quantity in grams.
- Calculating the price based on the quantity and price per kilogram.
- Applying a discount if the user chooses to pay in cash.
- Displaying the total cost to the user.

Key files:
- `Main.xaml`: The main workflow for the candy vending machine process.
- `ApskaiciuotiKaina.xaml`: A separate workflow for calculating the price of the selected candy.

## 3LD_Excel

This project processes Excel files and performs data manipulation. The workflow includes:
- Reading data from Excel files in the `Dokumentai` folder.
- Merging data from multiple files into a single DataTable.
- Filtering the data to include only specific rows (e.g., vegetables).
- Adding a calculated column for total price.
- Writing the processed data to an Excel file in the `Rezultatai` folder.
- Creating a formatted table and a pivot table for summary data.

Key files:
- `Main.xaml`: The main workflow for processing Excel files.

## 4LD_VartotojoSasaja

This project interacts with a web application (ACME System) and processes user data. The workflow includes:
- Logging into the ACME System using the Edge browser.
- Performing actions on the ACME website.
- Writing data to Excel sheets (`Kandidatai` and `WorkItems`).
- Processing the Excel file using an Excel Process Scope.

Key files:
- `Main.xaml`: The main workflow for interacting with the ACME System and processing data.
