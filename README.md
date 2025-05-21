# Robotic Process Automation

This repository contains automation workflows created using UiPath Studio. Each project showcases how RPA can handle repetitive tasks efficiently by interacting with files, websites, and user interfaces.

## linkedin-job-scraper

This project automates the process of searching for jobs on LinkedIn based on user-defined criteria. The workflow:
- Prompts the user to select or enter:
  - The desired job field (converted to English for search consistency).
  - A preferred salary range (as a tuple of minimum and maximum values).
  - The city for job search (from a list or entered manually; if "Nesvarbu" is selected, the city filter is left blank).
- Validates all user inputs for correctness and prompts to retry if values are missing or invalid.
- Handles all exceptions and displays clear error messages if something goes wrong.
- Uses the gathered criteria to perform a job search on LinkedIn, applying the specified filters.
- Collects data on matching job postings (such as job title, company, location, and other relevant details).
- Outputs the results to a structured Excel file for further analysis or review.
- Saves the jobs on the LinkedIn website for easy access later.

## 2LD_SaldainiuAutomatas

This project simulates a candy vending machine. The workflow:
- Asks the user to select a candy type and enter the amount in grams.
- Calculates the price based on a fixed rate per kilogram.
- Applies a discount if the user chooses to pay in cash.
- Displays the final price.

**Key files:**
- `Main.xaml`: Main logic for user interaction and price display.
- `ApskaiciuotiKaina.xaml`: Reusable component that handles price and discount calculation.

## 3LD_Excel

This project automates processing multiple Excel files. The workflow:
- Reads all `.xlsx` files from the `Dokumentai` folder.
- Merges their content into one DataTable.
- Filters specific data (e.g., vegetables).
- Calculates totals using expressions.
- Outputs the final result to an Excel file in the `Rezultatai` folder.
- Applies table formatting and generates a pivot table.

## 4LD_VartotojoSasaja

This automation interacts with the ACME test website to extract structured data. The robot:
- Logs into the system via browser.
- Navigates between sections such as Employees and Work Items.
- Extracts data from tables.
- Saves everything to Excel (`Kandidatai`, `WorkItems` sheets).

## 5LD_DarbasSuTinklalapiais

This project automates data gathering from IMDb using movie titles from Excel. The workflow:
- Opens IMDb and keeps the same browser session throughout.
- Reads movie titles from `Filmai.xlsx`.
- For each movie:
  - Searches the title on IMDb.
  - Selects the most relevant result.
  - Extracts info like release year, IMDb rating, popularity rank, and change.
  - Determines whether popularity has increased or decreased.
  - Returns to the main page before moving to the next title.
- Updates the Excel file with all the results and applies formatting.

**Key files:**
- `Main.xaml`: Full logic for reading, navigating, extracting, and writing data.
- `Filmai.xlsx`: Excel file with input/output structure for movies.

## 6LD_DarbasSuPDF

This automation processes PDF invoices and responds via email using dynamic content. The robot:
- Monitors the inbox for an email containing PDF invoices and a response template.
- Automatically saves all attachments into a newly created `Priedai` folder.
- Opens each invoice and extracts the invoice number, date, subtotal, and total amount due using screen scraping and OCR.
- Collects this data into a structured DataTable.
- After all invoices are processed, writes the results to a formatted Excel file.
- Loads the response template (`laiskas.txt`), customizes it with the extracted data, and sends a reply email to the original sender.
- Attaches the filled-out Excel summary to the response email.

