# Data Cleaning Log & Methodology

**Dataset:** Online Retail II (UCI Machine Learning Repository)
**Platform:** Google Sheets
**Original Size:** ~500,000 Rows
**Sampled Size:** 15,000 Rows (Stratified Sample)

---

## 1. Data Sourcing & Sampling Strategy

**Constraint:** The original dataset exceeded the processing limits of the mandatory platform (Google Sheets), causing calculation timeouts.
**Action:** We performed a strategic truncation to retain the first **15,000 rows**.
**Justification:** This sample size satisfies the student handbook requirement (>5,000 rows) while ensuring the dashboard remains interactive and "lag-free" for the final presentation.

---

## 2. Data Dictionary & Cleaning Log (Tab 2)

*This table tracks all modifications made to the raw data to ensure Data Quality.*

| Column Name           | Original Issue                           | Cleaning Action Taken           | Rationale / Logic                                                                                                                        |
| :-------------------- | :--------------------------------------- | :------------------------------ | :--------------------------------------------------------------------------------------------------------------------------------------- |
| **Customer ID** | Contains ~22% Null values.               | **Imputed with "Guest".** | To prevent data loss. "Guest" allows us to track non-member revenue without skewing member metrics.                                      |
| **Quantity**    | Contains negative values (e.g., -12).    | **Filtered & Moved.**     | Negative values represent Returns. We moved these to a separate 'Returns_Analysis' tab to prevent them from canceling out Gross Revenue. |
| **StockCode**   | Contains operational junk ('POST', 'M'). | **Deleted Rows.**         | Codes like 'POST' (Postage) and 'M' (Manual) are service fees, not retail products.                                                      |
| **StockCode**   | Contains Blank/Null values.              | **Deleted Rows.**         | A transaction without a product code is invalid and cannot be categorized.                                                               |
| **Description** | Contains Blank/Null values.              | **Deleted Rows.**         | Rows with missing product names cannot be visualized in "Top Products" charts.                                                           |

---

## 3. Detailed Execution Steps

### Step 1: Handling Missing Customer IDs

* **Problem:** Large volume of blank cells in `Customer ID` column.
* **Execution:** Used `Find & Replace` (Ctrl+H) to replace all empty cells in the column with the string `Guest`.
* **Impact:** Ensures 100% data density for the "Customer" dimension.

### Step 2: Isolating Cancellations (Returns)

* **Problem:** The `Quantity` column mixed Sales (positive) and Returns (negative).
* **Execution:** 1. Filtered `Quantity < 0`.
  2. Extracted these rows to a new tab named **"Returns_Analysis"**.
  3. Deleted them from the main **"Analysis"** tab.
* **Impact:** Allows for accurate calculation of "Gross Revenue" while preserving return data for separate "Leakage" analysis.

### Step 3: Removing "Junk" Codes

* **Problem:** Non-product codes were present (`POST`, `M`, `D`, `BANK CHARGES`).
* **Execution:** Applied a manual filter to select and delete these specific codes.
* **Impact:** Cleans the "Average Order Value" metric by removing non-retail fees.

### Step 4: Removing Invalid Blanks

* **Problem:** Rows existed with `StockCode = Null` or `Description = Null`.
* **Execution:** Deleted these rows entirely.
* **Impact:** Removes "orphan" data that would otherwise appear as "(blank)" in dashboard charts.
