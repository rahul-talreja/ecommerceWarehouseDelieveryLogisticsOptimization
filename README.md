📦 Optimizing Delivery Logistics for E-Commerce Warehouses
📌 Project Overview

In the fast-growing e-commerce industry, efficient delivery logistics are critical for minimizing operational costs while maintaining high customer satisfaction. Delays, inefficient shipment mode selection, and suboptimal warehouse utilization can significantly impact profitability and service quality.

This project focuses on optimizing delivery logistics for e-commerce warehouses by combining predictive analytics and prescriptive optimization. Using a real-world dataset, we analyze shipment modes, warehouse blocks, product characteristics, and customer behavior to:

Predict on-time delivery outcomes

Optimize shipment mode allocation to minimize total delivery costs

Improve operational efficiency and sustainability

🎯 Objectives

Minimize total delivery costs while ensuring on-time delivery

Identify factors contributing to delivery delays

Improve delivery prediction accuracy using machine learning

Recommend optimal shipment modes and logistics strategies to enhance customer satisfaction

📊 Dataset

Source: Kaggle – Customer Analytics Dataset

Link: https://www.kaggle.com/datasets/prachi13/customer-analytics/data

Key Features:

Warehouse block

Mode of shipment (Ship, Road, Air)

Product importance

Cost of product

Discount offered

Weight (grams)

Customer care calls

Customer rating

Prior purchases

Gender

Reached on Time (target variable)

This dataset supports both predictive modeling and logistics optimization use cases.

🔍 Problem Formulation
Objective Function

The primary objective is to minimize total delivery cost while meeting customer demand and operational constraints:

Minimize 
𝐶
𝑡
𝑜
𝑡
𝑎
𝑙
=
(
𝐶
𝑆
ℎ
𝑖
𝑝
⋅
𝑄
𝑆
ℎ
𝑖
𝑝
)
+
(
𝐶
𝑅
𝑜
𝑎
𝑑
⋅
𝑄
𝑅
𝑜
𝑎
𝑑
)
+
(
𝐶
𝐴
𝑖
𝑟
⋅
𝑄
𝐴
𝑖
𝑟
)
Minimize C
total
	​

=(C
Ship
	​

⋅Q
Ship
	​

)+(C
Road
	​

⋅Q
Road
	​

)+(C
Air
	​

⋅Q
Air
	​

)

Where:

𝐶
C = Cost per shipment mode

𝑄
Q = Quantity shipped via each mode

🔢 Decision Variables

XShip, XRoad, XAir – Binary variables indicating selection of shipment mode

QShip – Quantity shipped by ship (200 units)

QRoad – Quantity shipped by road (500 units)

QAir – Quantity shipped by air (0 units)

⚙️ Constraints

The optimization model incorporates real-world logistics limitations:

Warehouse capacity constraints to prevent congestion

Delivery time windows to ensure on-time delivery

Shipping mode constraints (cost, time, and weight limits)

Demand fulfillment ensuring all customer orders are met

Operational variability (traffic, weather, third-party delays)

These constraints ensure the model remains realistic and actionable.

📈 Predictive Analytics
Models Used

Random Forest

Logistic Regression

Evaluation Metrics

Accuracy

AUC (Area Under the ROC Curve)

Precision, Recall, F1-score

Confusion Matrix

Model Performance
Model	Accuracy	AUC
Random Forest	66.6%	0.746
Logistic Regression	63.7%	0.725

Key Insight:
Random Forest outperformed Logistic Regression in both accuracy and AUC, particularly in identifying delayed deliveries (Class 1), making it more suitable for operational decision-making.

📦 Prescriptive Analytics (Optimization)
Key Findings

Road transport: 100% capacity utilization (high efficiency)

Ship transport: ~67% utilization (opportunity for consolidation)

Air transport: Excluded due to high costs and low economic feasibility

Sensitivity Analysis

Road and ship are the most cost-effective shipment modes

Air shipping is economically unviable under current cost structures

Increasing shipping capacity marginally improves objective outcomes

📊 Shipment Mode Performance Analysis

Ship: Highest volume and best on-time performance

Road: Balanced but variable performance; prone to delays

Air: Low volume with disproportionately high delays

This analysis highlights ship transport as the most reliable mode, while road and air shipments require operational improvements.

⚖️ Trade-Off Analysis

Cost vs. Speed: Lower-cost modes may reduce delivery reliability

Efficiency vs. Sustainability: Cost-efficient modes may increase environmental impact

Capacity vs. Flexibility: Increasing capacity adds cost but improves demand responsiveness

Accuracy vs. Interpretability: Random Forest is more accurate, Logistic Regression is more interpretable

🧠 Key Results & Insights

High utilization rates are critical for minimizing logistics costs

Underutilized shipping capacity represents cost-saving opportunities

Predictive analytics improves shipment planning and demand alignment

Combining predictive and prescriptive approaches leads to better operational decisions

🚀 Future Recommendations

Further optimize road and ship transportation costs

Improve air shipping feasibility through cost restructuring

Retrain predictive models with updated data

Integrate real-time demand forecasting

Incorporate sustainability metrics into optimization decisions

🛠 Tools & Technologies

Python

pandas, NumPy

scikit-learn

Matplotlib, Seaborn

Linear Programming / Optimization techniques

Google Colab

📎 Project Resources

Colab Notebook:
https://colab.research.google.com/drive/1YKdbvgAbAQdLonLLLm2XxfWmAIP5AUMv

Dataset:
https://www.kaggle.com/datasets/prachi13/customer-analytics/data
