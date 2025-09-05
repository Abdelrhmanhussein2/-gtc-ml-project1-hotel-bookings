# Hotel Booking Demand - Data Cleaning & Feature Engineering

## 📌 Project Overview
This project analyzes and preprocesses the **Hotel Booking Demand dataset**.  
The goal is to clean the data, handle missing values, remove outliers, and engineer useful features to prepare the dataset for predictive modeling.

---

## 📂 Deliverables
1. **notebook.ipynb** → Jupyter Notebook containing all preprocessing steps, EDA, and feature engineering.  
2. **cleaned_data.csv** → Final cleaned dataset after handling missing values, encoding, and outlier treatment.  
3. **report.md** → Documentation of main findings and data quality issues.

---

## 🛠️ Preprocessing Steps
- **Missing Values Handling**  
  - Filled categorical features with mode.  
  - Filled numerical features with median/mode as appropriate.  
  - Dropped uninformative columns like `company`.  

- **Data Type Fixing**  
  - Converted date columns into proper datetime format.  

- **Feature Engineering**  
  - `total_guests` = adults + children + babies  
  - `total_nights` = stays_in_weekend_nights + stays_in_week_nights  
  - `is_family` = binary flag for bookings with children/babies  

- **Encoding**  
  - One-Hot Encoding for low-cardinality categorical features (`meal`, `market_segment`, `distribution_channel`).  
  - Frequency Encoding for `country` (rare values grouped into "Other").  

- **Outlier Handling**  
  - Applied IQR method (either removal or capping).  

- **Data Leakage Prevention**  
  - Dropped `reservation_status` and `reservation_status_date`.  

- **Final Split**  
  - Dataset split into Train/Test (80/20).  

---

## 📊 Dataset Shapes
- Before Cleaning: **119,390 rows, 36 columns**  
- Or preserved all rows using capping method.  

---

