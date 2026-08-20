# E-commerce-dataset
Merging Orders, Customers &amp; Products datasets with Pandas — merge(), concat(), apply(), and DateTime feature engineering into one clean processed CSV.
# 🛍️ Processed E-Commerce Dataset

A Python & Pandas notebook that integrates three related e-commerce data sources — **Orders**, **Customers**, and **Products** — into a single clean, analysis-ready dataset using `merge()`, `concat()`, `apply()`, and DateTime operations.

## 📁 Files

| File | Description |
|---|---|
| `Processed_Ecommerce_Dataset.ipynb` | Main notebook: loading, merging, feature engineering, and export |
| `Day9_Orders.csv` | Raw orders data (input) |
| `Day9_Customers.csv` | Raw customer data (input) |
| `Day9_Products.csv` | Raw product data (input) |
| `Processed_Ecommerce_Dataset.csv` | Final combined & processed dataset (output) |

## 📊 Source Data

- **Orders** — `Order_ID`, `Order_Date`, `Customer_ID`, `Product_ID`, `Quantity`, `Payment_Method`, `Order_Status`
- **Customers** — `Customer_ID`, `Customer_Name`, `City`, `Region`, `Membership_Type`
- **Products** — `Product_ID`, `Product_Name`, `Category`, `Unit_Price`, `Brand`

## 🔍 What the Notebook Does

- **Loading** — reads all three CSVs into Pandas DataFrames
- **Merging (`merge()`)** — joins Orders → Customers → Products on their ID keys into one unified table
- **Combining (`concat()`)** — demonstrates stacking/recombining DataFrames (e.g. splitting by customer membership tier and reassembling)
- **DateTime operations** — converts `Order_Date` to datetime and extracts month, day, day-of-week, week number, and a weekend flag
- **Feature engineering (`apply()`)** — creates derived columns:
  - `Total_Amount` (Quantity × Unit_Price)
  - `Order_Value_Segment` (Low / Medium / High)
  - `Customer_Name_Initials`
  - `Is_Delivered` (boolean flag)
- **Final dataset** — reorganizes everything into a clean, logically ordered DataFrame
- **Export** — saves the result as `Processed_Ecommerce_Dataset.csv`

## 🛠️ Tools Used

- Python
- Pandas
- NumPy
- Jupyter / Google Colab

## 🚀 How to Run

1. Open `Processed_Ecommerce_Dataset.ipynb` in [Google Colab](https://colab.research.google.com/) or Jupyter Notebook.
2. Upload `Day9_Orders.csv`, `Day9_Customers.csv`, and `Day9_Products.csv` to the same environment (or update the file paths in the first code cell).
3. Run all cells (`Runtime > Run all` in Colab).
4. The processed file `Processed_Ecommerce_Dataset.csv` will be generated in the working directory.

## 📌 Key Insights

- Orders, customers, and products merge cleanly on their ID keys with no data loss.
- Order activity varies by month and day of the week, useful for demand planning.
- Orders split naturally into Low/Medium/High value segments.
- Delivery status can be tracked as a simple boolean flag for quick success-rate analysis.
