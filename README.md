# Bank Customer Segmentation & Risk Profiling

## Executive Summary
This project leverages K-Means Clustering to segment a digital bank's customer base into four strategic personas. By analyzing demographic data and credit behavior, the analysis aims to balance portfolio growth with risk management.

The segmentation reveals critical insights for a digital-first banking strategy: identifying a high-volume segment ideal for **Buy Now Pay Later (BNPL)** products and a high-risk segment requiring **manual underwriting**. The proposed hybrid-automation strategy allows the bank to automate loan approvals for 80% of applicants while strictly controlling the high-value risk exposure in the remaining 13%.

## 1. Project Background
In the competitive landscape of digital banking, a "one-size-fits-all" approach leads to inefficient marketing and increased credit risk.
**Objective:**
* To perform Behavioral Segmentation using unsupervised machine learning.
* To identify distinct customer profiles for hyper-personalized product recommendations (BNPL vs. Wealth Management).
* To design a tiered risk management strategy based on cluster characteristics.

**Methodology:**
* **Algorithm:** K-Means Clustering.
* **Validation:** Elbow Method & Silhouette Analysis.
* **Data Processing:** Log transformation for skewed financial data and Standardization (StandardScaler).

## 2. Customer Personas (Cluster Analysis)
The analysis identified four distinct customer segments, each requiring a unique business approach.

<img width="1034" height="633" alt="scatter_segmentation" src="https://github.com/user-attachments/assets/78d6927b-0d36-45b6-be0e-ba070e9bbd41" />


### Cluster 0: The Conservative Seniors (Wealth Management Target)
* **Profile:** Older demographic with the strongest saving profile.
* **Behavior:** Low borrowing frequency, high liquidity.
* **Strategy:** Avoid aggressive lending offers. Focus on **Wealth Management**, deposits, and retirement investment products.

### Cluster 1: The Mainstream Borrowers (Growth Engine)
* **Profile:** Active borrowers with moderate credit needs.
* **Behavior:** High demand for vehicle loans (Car).
* **Strategy:** Target for **Digital Vehicle Loans (KKB)** with instant approval processes to capture market share.

### Cluster 2: The PayLater Users (Volume Driver)
* **Profile:** Younger demographic, tech-savvy, low savings balance ('little').
* **Behavior:** High frequency of small-ticket loans, primarily for electronics (Radio/TV).
* **Strategy:** This segment validates the need for a **Buy Now Pay Later (BNPL)** feature. Risk control should rely on real-time transaction scoring and strict limit management rather than traditional collateral.

### Cluster 3: The High-Stakes Borrowers (Risk Watchlist)
* **Profile:** Borrowers with high loan amounts but poor saving history (28% unknown savings).
* **Risk Level:** **High**. Despite their high value, they represent the largest potential for default.
* **Strategy:** **Manual Underwriting**. Exclude from auto-approval pipelines. Every application must be reviewed by a credit analyst.

## 3. Strategic Business Recommendations
Based on the segmentation, the following actions are recommended for the product and risk teams:

1. **Hybrid-Automation Approval Policy:**
   * **Automate (80%):** Implement auto-approval workflows for Clusters 0, 1, and 2 (Low/Medium volume) to ensure speed and user experience.
   * **Manual Review (13%):** Flag all applications from Cluster 3 for manual verification to mitigate large-scale NPL (Non-Performing Loan) risk.

2. **Product Hyper-Personalization:**
   * **App Interface for Cluster 2:** Customize the homepage to highlight "Gadget Installments" and cashback promos.
   * **App Interface for Cluster 0:** Prioritize "Deposito Bunga Spesial" and investment educational content.

3. **Digital Auto Loan (KKB) Expansion:**
   * Since demand for car loans dominates Clusters 0, 1, and 3, the bank should accelerate the development of an end-to-end digital car loan product to serve this cross-segment demand.

## Tools & Libraries Used
* **Python:** Programming Language.
* **Scikit-Learn:** K-Means Clustering, StandardScaler.
* **Pandas & NumPy:** Data Manipulation.
* **Seaborn & Matplotlib:** Data Visualization (Histograms, Boxplots).

---
