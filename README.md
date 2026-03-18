# Supply Chain Exploratory Data Analysis (EDA)

## Project Objective

This project analyzes operational patterns in a supply chain dataset containing **4,500 order records** to uncover insights into:

- Warehouse workload distribution  
- Order size patterns  
- Lead time behavior  
- Shipping delay patterns  
- Supplier performance  
- Product distribution across warehouses  

The goal is to generate **actionable insights** for inventory planning, warehouse allocation, and delivery efficiency.

---

## Tools Used

- Python  
- Pandas  
- Matplotlib  
- Seaborn  
- Power BI  

---

## Dataset Overview

The dataset contains **4,500 supply chain transactions** with 8 variables.

| Variable           | Description                          |
|-------------------|--------------------------------------|
| OrderID           | Unique order identifier              |
| ProductID         | Product code                         |
| Warehouse         | Warehouse fulfilling the order       |
| OrderQuantity     | Quantity ordered                     |
| LeadTimeDays      | Processing lead time                 |
| ShippingDelayDays | Shipment delay duration              |
| SupplierRating    | Supplier performance rating          |
| OrderDate         | Date order was placed                |

**Data Types:**  
- Numerical: OrderID, ProductID, OrderQuantity, LeadTimeDays, ShippingDelayDays, SupplierRating  
- Categorical: Warehouse  
- Date: OrderDate  

---

## Data Quality Assessment

**Missing Values:**

| Variable       | Missing Values |
|----------------|----------------|
| SupplierRating | 149            |

**Treatment:**  
- Missing values replaced with **mean supplier rating (2.98)** to preserve dataset size and maintain overall distribution.

---

## Order Quantity Analysis

| Statistic         | Value |
|------------------|-------|
| Mean              | 251.87 |
| Median            | 248 |
| Standard Deviation| 141.42 |
| Minimum           | 10 |
| Maximum           | 499 |

**Percentiles:**

| Percentile | Quantity |
|------------|---------|
| 25%        | 130     |
| 50%        | 248     |
| 75%        | 374     |

**Insight:**  
- 50% of orders fall between 130 and 374 units  
- System primarily handles **medium-to-large orders**, optimized for bulk transactions  

---

## Warehouse Order Distribution

| Warehouse  | Orders | Percentage |
|------------|--------|------------|
| Abuja_WH   | 1523   | 33.8%      |
| Lagos_WH   | 1520   | 33.7%      |
| Kano_WH    | 1457   | 32.4%      |

**Insight:**  
- Order allocation is **balanced across warehouses**  
- Effective load balancing ensures **no warehouse is overloaded**  

---

## Lead Time Analysis

| Statistic          | Value |
|-------------------|-------|
| Mean               | 14.92 days |
| Median             | 15 days |
| Minimum            | 1 day |
| Maximum            | 29 days |
| Std Dev            | 8.36 |

**Percentiles:**

| Percentile | Lead Time |
|------------|-----------|
| 25%        | 8 days    |
| 50%        | 15 days   |
| 75%        | 22 days   |

**Insight:** Lead times are **stable and predictable**, reflecting consistent internal processing efficiency.  

---

## Shipping Delay Analysis

| Statistic          | Value |
|-------------------|-------|
| Mean               | 4.46 days |
| Median             | 4 days |
| Minimum            | 0 days |
| Maximum            | 9 days |
| Std Dev            | 2.85 |

**Insight:**  
- 50% of deliveries delayed **2–7 days**  
- Delays are moderate but consistent, suggesting **system-wide logistics issues**  

**Shipping Delay by Warehouse:**

| Warehouse | Average Delay |
|-----------|---------------|
| Abuja     | 4.46 days     |
| Lagos     | 4.46 days     |
| Kano      | 4.47 days     |

- Maximum difference ? 0.01 days  
- Indicates **standardized logistics processes** across warehouses  

---

## Supplier Rating Analysis

| Statistic | Value |
|-----------|-------|
| Mean      | 2.98  |
| Median    | 3     |
| Minimum   | 1     |
| Maximum   | 5     |
| Std Dev   | 1.15  |

**Supplier Rating vs Shipping Delay:**  
- Correlation r = 0.007 ? **no meaningful relationship**  

**Insight:**  
- Shipping delays are likely driven by **transportation infrastructure, warehouse efficiency, logistics coordination, and external factors** rather than supplier performance  

---

## Correlation Analysis

| Variables                       | Correlation |
|--------------------------------|-------------|
| OrderQuantity vs LeadTime       | 0.03        |
| OrderQuantity vs ShippingDelay | -0.01       |
| LeadTime vs ShippingDelay       | -0.02       |
| SupplierRating vs ShippingDelay | 0.007       |

**Observation:**  
- All correlations are **extremely weak**, indicating operational variables behave largely independently  

---

## Operational Insights

1. **Balanced Warehouse Utilization** – orders distributed evenly  
2. **Bulk-Oriented Operations** – medium-to-large order sizes dominate  
3. **Stable Processing Times** – predictable lead times  
4. **Systemic Shipping Delays** – uniform across warehouses  
5. **Supplier Ratings Do Not Drive Delays** – logistics factors dominate  

---

## Business Recommendations

1. **Investigate Logistics Bottlenecks:** Focus on transportation networks, delivery routing, and carrier performance  
2. **Enhance Delivery Performance Monitoring:** Track route efficiency, delivery distances, and carrier reliability  
3. **Leverage Predictable Demand Patterns:** Improve inventory planning, workforce allocation, and procurement scheduling  

---


## Project Files

[EDA Notebook](https://github.com/Adedayo-MyData/Supply-Chain-Exploratory-Data-Analysis/blob/main/Supply%20Chain%20EDA%20%20Using%20Python.ipynb)– Data preprocessing and exploratory analysis  


---

## Conclusion

The analysis reveals a **well-balanced and operationally stable supply chain** with:

- Evenly distributed workloads  
- Consistent processing times  

**Opportunity:** Shipping delays are uniform and **not driven by supplier performance**, suggesting **logistics and transportation factors** as the primary constraint.  

**Recommendation:** Addressing external bottlenecks can significantly improve supply chain efficiency.  

---

## Author

**Adedayo Adebayo**  
Data Scientist | Business Analyst

