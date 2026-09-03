# SpendDNA - your wallet's year-end story. 

SpendDNA is a Python-based data processing and financial analytics tool designed to parse, categorize, and analyze raw bank or UPI transaction statements (such as PhonePe CSV exports). It transforms unorganized statement data into actionable financial insights, spending habits, anomaly flags, and predictive forecasts.

---

## Key Features

* **Flexible Data Parsing:** Automatically handles non-standard CSV headers, variable date/time formats, and currency formatting (e.g., removing `₹`, `Rs.`, and commas).
* **Smart Vendor & Category Mapping:** Uses string-matching logic tailored to UPI payment descriptions (e.g., "Paid to...", "Received from...") to classify transactions across categories like Education, Food Delivery, E-commerce, Utilities, Groceries, and P2P Transfers.
* **Executive Financial Summary:** Calculates core financial health metrics, including Total Income/Credits, Total Debits, Net Cash Flow, and Savings Rate.
* **Spending Archetypes:** Identifies user spending habits based on proportion of expenditure (e.g., *Academic Spender*, *Shopper*, *P2P Transferer*).
* **Anomaly Detection:** Flags irregular high-value transactions using statistical Z-Score logic ($\ge 3.0$ standard deviations from the category mean).
* **Spend Forecasting:** Predicts next month's category-wise expenses using a NumPy-based rolling average analysis.
* **Day-of-Week Insights:** Highlights spending patterns by contrasting average weekday versus weekend expenditures.
* **Vendor Cleanup Audit:** Logs any unmapped or uncategorized transaction descriptions for rule refinement.

---

## Tech Stack & Dependencies

* **Language:** Python 
* **Core Libraries:**
  * `pandas`: Data loading, cleaning, grouping, and matrix operations.
  * `numpy`: Array manipulations, matrix calculations, standard deviation logic, and forecasting.

---

## sample out of MY_STATEMENT
<img width="1301" height="794" alt="report" src="https://github.com/user-attachments/assets/dc2e5439-23c9-44a3-ba79-ddb515b2b77b" />


