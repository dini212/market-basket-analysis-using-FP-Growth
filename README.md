# Application of the FP-Growth Algorithm for Market Basket Analysis on Online Retail Transaction Data

## 📌 Project Overview
This project aims to analyze customer purchasing patterns from the *Online Retail II* dataset (2010–2011) using the **FP-Growth** algorithm. The findings support data-driven business strategies, including product bundling, cross-selling recommendation engine designs, and optimized product layout planning.

## 🛠️ Tools & Libraries
- **Language**: Python 3
- **Core Libraries**: `pandas`, `numpy`, `matplotlib`, `mlxtend` (TransactionEncoder, fpgrowth, association_rules)

## 📊 Data Cleaning & Analysis Workflow
1. **Data Preprocessing**:
   - Removed canceled transactions (Invoice 'C').
   - Filtered out invalid records (`Quantity > 0` and `Price > 0`).
   - Excluded non-product entries (e.g., POST, DOT, etc.).
   - **Clean dataset total**: 527,758 rows across 19,773 unique clean invoices.
2. **FP-Growth Modeling**:
   - Parameters: `MIN_SUPPORT = 0.01` (1%), `MIN_CONFIDENCE = 0.50`, `LIFT > 1`.
   - Generated **2,026 frequent itemsets** and **962 association rules** (870 unique rules).
3. **Robustness (Sensitivity) Testing**:
   - 506 unique rules (58.2%) persisted even after removing the top 1% largest invoices (wholesale buyer segment), confirming model robustness.

## 💡 Key Insights & Business Recommendations
- **Herb Marker Set**: Variant combinations of *Herb Markers* (Thyme, Rosemary, Parsley) showed exceptionally strong associations with a *lift* of ~73–77 and *confidence* of ~89–93%.
- **Regency Collection**: *Tea Plate* and *Sugar Bowl → Milk Jug* demonstrated high co-purchase relationships.
- **Strategic Recommendations**:
  - Implement rule-based product bundles leveraging robust association rules.
  - Optimize store layout/placement by positioning frequently co-purchased items close to each other (including cross-category rules).
*Disediakan oleh: Dwi Rahmadini*
