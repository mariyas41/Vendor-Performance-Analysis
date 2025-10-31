# 🏬 Vendor Performance Analysis Dashboard

### 🎯 Objective
To analyze vendor performance and profitability trends for a retail company by integrating **BigQuery**, **Python**, and **Power BI**.  
The goal was to identify top and underperforming vendors, optimize purchase planning, and improve profit margins.

---

### 🧰 Tools & Technologies
- **BigQuery (SQL)** – Data extraction and aggregation from cloud storage  
- **Python (EDA & Preprocessing)** – Exploratory data analysis, cleaning, and outlier handling  
- **Power BI** – Data modeling, DAX calculations, and interactive visualization  
- **Excel/CSV** – Intermediate data export and metadata review  

---

### 📊 Dashboard
📂 [Open Report Folder](./Report)  
➡️ [Download Power BI Report (.pbix)](https://drive.google.com/your-link-here)

![Dashboard Preview](./Reports/dashboard_preview.png)

> The interactive Power BI dashboard visualizes vendor-level KPIs, brand contributions, sales vs. purchase trends, and unsold stock value.  
> It enables procurement teams to make data-driven vendor and product decisions.

---

### 🎞️ Presentation
📂 [Open Presentation Folder](./Presentation)  
➡️ [Download Presentation (.pptx)](./Presentation/Vendor_performance_ANALYSIS.pptx)

---

### 🔍 Project Overview
The dataset includes **sales, purchase, and stock details** for multiple brands and vendors.  
The aim was to:
- Identify **top-performing vendors and brands**  
- Highlight **underperforming brands** needing marketing or stock adjustment  
- Track **profit, sales, and unsold inventory** trends over time  

---

### 🧩 Key Analytical Steps

1. **Data Extraction (BigQuery)**
   - Queried transactional data (Sales, Purchase, Inventory)  
   - Joined and aggregated across Vendor, Brand, and Category tables  

2. **Data Cleaning & EDA (Python)**
   - Handled missing purchase prices and negative profit anomalies  
   - Verified SKU-level consistency  
   - Generated summary statistics for margin, stock, and turnover rate  

3. **Data Modeling (Power BI)**
   - Created star schema linking Vendor, Brand, and Date dimensions  
   - Calculated DAX metrics:
     - `Total Purchase` = SUM(Purchase[Amount])  
     - `Total Sales` = SUM(Sales[Amount])  
     - `Profit` = [Total Sales] - [Total Purchase]  
     - `Margin %` = DIVIDE([Profit], [Total Sales])  
     - `Unsold Capital` = Stock[Qty] * Purchase[Unit Cost]  

4. **Visualization**
   - Sales vs. Profit comparison by Vendor  
   - Top 10 Brands by Revenue  
   - Vendor contribution share  
   - Unsold Stock trend over time  
   - Profit margin analysis by brand  

---

### 💡 Insights

| Observation | Insight | Business Impact |
|--------------|----------|----------------|
| Vendor performance highly skewed | Top 5 vendors contribute ~70% of total revenue | Focus on vendor relationship management and discount leverage |
| Profit margin inconsistency | Some brands show negative margins despite high sales | Indicates over-purchasing or pricing inefficiency |
| Unsold capital value significant | ~25% of stock remains unsold for >60 days | Inventory holding cost can be reduced with better forecasting |
| Low-performing brands | Identified via DAX threshold filters | Recommend targeted marketing or vendor negotiation |

---

### 🧠 Recommendations
- **Optimize Procurement:** Negotiate with high-volume vendors for better discounts.  
- **Control Overbuying:** Monitor unsold stock and tie reorder quantity to historical demand.  
- **Promote Weak Brands:** Run targeted campaigns for low-margin but high-stock brands.  
- **Automate Alerts:** Build Power BI KPI thresholds to flag vendors below target margins.

---

### 🚀 Outcomes
✅ Improved visibility into vendor-wise profitability and contribution.  
✅ Identified brands for potential promotion or delisting.  


---

### 🖱️ Dashboard Interactivity
- **Filters & Slicers:** Brand, Vendor, Category, and Time Period  
- **Dynamic KPIs:** Adjust instantly with filters  
- **Drill-Through:** Explore vendor details with margin and stock breakdown  
- **Cross-Filtering:** Clicking visuals updates all others for contextual analysis  



---

### 🗂️ Repository Structure
