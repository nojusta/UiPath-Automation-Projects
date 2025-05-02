# Robotic Process Automation

This repository contains automation workflows created using UiPath Studio. Each project demonstrates practical use cases of RPA by automating repetitive tasks across different data sources, websites, and interfaces.

## 2LD_SaldainiuAutomatas

This project simulates a candy vending machine process. The workflow:
- Asks the user for the type and quantity (in grams) of candy.
- Calculates the price based on a set price per kilogram.
- Applies a discount if payment is in cash.
- Displays the total cost to the user.

**Key files:**
- `Main.xaml`: The main workflow for the vending machine logic.
- `ApskaiciuotiKaina.xaml`: A reusable workflow for price calculation.

## 3LD_Excel

This project automates Excel file processing and summarization. The workflow:
- Reads multiple Excel files from the `Dokumentai` folder.
- Merges data into a single DataTable.
- Filters data (e.g., selects only vegetables).
- Calculates total prices using expressions.
- Outputs the result to an Excel file in the `Rezultatai` folder.
- Formats the result as a table and generates a pivot table.

## 4LD_VartotojoSasaja

This project interacts with the ACME test system website and extracts user and task data. The workflow:
- Logs into the ACME system through a browser.
- Navigates through different sections of the system (e.g., Employees, Work Items).
- Extracts structured data from web pages.
- Saves and formats the results in Excel (`Kandidatai`, `WorkItems` sheets).

## 5LD_DarbasSuTinklalapiais

This project automates data collection from the IMDb website based on a list of movie titles in an Excel file. The workflow:
- Opens the IMDb website once and stays on the same browser session for all operations.
- Reads movie titles from `Filmai.xlsx` using `Read Range`.
- For each movie:
  - Searches the movie title using `Type Into`.
  - Clicks on the best matching result.
  - Extracts the release year, IMDb rating, popularity rank, and popularity change.
  - Determines whether the popularity increased or decreased.
  - Returns to the main IMDb page before processing the next movie.
- Writes the full results back into the original Excel file using `Write Range` and applies table formatting.

This project showcases dynamic data handling, browser automation, structured iteration, and adaptive logic within a single session.

**Key files:**
- `Main.xaml`: The complete workflow for reading from and writing to Excel, navigating IMDb, and extracting structured movie data.
- `Filmai.xlsx`: The input/output Excel file used for storing and updating movie information.
