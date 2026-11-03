# End-to-End Monthly Financial & Tax Accounting Model

## 📌 Project Overview
This project is a fully automated, comprehensive Excel-based financial accounting system that mirrors the exact monthly cycle of an Indian trading business. It demonstrates advanced proficiency in double-entry bookkeeping, tax compliance (GST & TDS), bank reconciliation, and final financial reporting using Advanced Excel formulas.

## 🛠️ Architecture & Workflow
The workbook is divided into six interconnected modules, utilizing dynamic lookups and conditional logic to ensure zero-error balancing:

1. **Chart of Accounts (Master Data)**
   - Structured list of all general ledgers mapped to their Account Types (Asset, Liability, Equity, Income, Expense) and normal balances.
   - Utilizes Data Validation to ensure clean data entry in the journal.

2. **General Journal Register**
   - Contains 80+ realistic dummy transactions for a 30-day business cycle.
   - Accurately tracks Intra-state (CGST/SGST) and Inter-state (IGST) sales and purchases.
   - Includes TDS deductions on professional fees (Sec 194J) and commercial rent (Sec 194I).

3. **Dynamic Trial Balance**
   - Built using automated `SUMIFS` targeting the Journal Register.
   - Self-auditing mechanism verifies that Net Debits equal Net Credits exactly down to the decimal.

4. **GST Computation (GSTR-3B Sandbox)**
   - Extracts Output Tax Liability from sales and Eligible Input Tax Credit (ITC) from purchases and freight.
   - Automatically calculates the Net GST Payable via Electronic Cash Ledger.

5. **Automated Bank Reconciliation Statement (BRS)**
   - Compares the Cash Book (Bank Ledger) against a simulated Bank Statement.
   - Uses `MATCH` and `ISNUMBER` arrays to instantly flag unpresented cheques, uncleared deposits, and unrecorded bank charges.

6. **Executive Financial Reports (Final Accounts)**
   - **Profit & Loss Statement**: Pulls revenue and COGS (Cost of Goods Sold) dynamically to output Gross Profit, followed by operating expenses to yield Net Profit.
   - **Balance Sheet**: Follows standard Schedule III structure, balancing Total Assets against Total Liabilities & Shareholder Equity. 

## 📊 Key Excel Skills Demonstrated
*   **Data Validation & Formatting**: Drop-down lists and Table Formatting (Ctrl+T) for robust data entry.
*   **Logical & Lookup Functions**: `VLOOKUP`, `IF`, `MAX`, `ISNUMBER`, and `MATCH` used extensively to link sheets and reconcile discrepancies.
*   **Advanced Aggregation**: Complex `SUMIFS` formulas used to extract specific tax parameters and generate the Trial Balance dynamically.

## 📥 How to Explore
Download the `.xlsx` file and test the interactivity. If you alter any transaction value in the **Journal_Transactions** tab, you will see the Trial Balance, GST Computation, and Balance Sheet instantly recalculate and balance themselves.
