# meal-delivery-optimization
Optimization model to reduce delivery time and improve route efficiency
# 🍽️ Meal Delivery Optimization Model (MDOM)

📦 **Project Type**: Operations Research & Excel-Based Optimization  
🎓 **Course**: DS 852 – Managerial Decision-Making, San Francisco State University  
👩‍💻 **Author**: Padmasree Sappa  
📁 Tools: Microsoft Excel, Solver, VBA Macros, Haversine Formula, Linear Programming  

---

## 🧠 Project Overview

Meal delivery services face growing pressure to fulfill customer orders quickly and cost-effectively. Challenges such as traffic congestion, courier availability, and poor assignments increase delivery times, reduce satisfaction, and inflate operational costs.

To address this, I developed the **Meal Delivery Optimization Model (MDOM)** — an Excel-based optimization solution using **Solver** and **VBA Macros**. MDOM assigns the best courier to each order using dynamic delivery-time estimates based on traffic, weather, distance, and courier speed.

> 🎯 Result: 15% average reduction in delivery time, balanced courier workloads, and fully automated optimization workflow.

---

## 🎯 Project Objectives

- Minimize **total delivery time** using optimization  
- Assign **each order exactly once**  
- Ensure **balanced courier workloads**  
- Incorporate **real-world factors** (traffic, weather, vehicle speed)  
- Enable **1-click automation** using Excel Macros

---

## 📊 Dataset & Engineered Features

**Raw Inputs:**
- Order IDs, Customer locations (lat/lon), Restaurant coordinates
- Courier IDs, vehicle type, rating, speed
- Order timestamps (placed, picked, delivered)
- Traffic and weather conditions

**Feature Engineering:**
- 🧮 Distance using the Haversine Formula  
- 🕓 Estimated delivery time = Prep Time + (Distance / (Speed × Weather × Traffic))
- Encoded traffic/weather text to numeric values for calculation  
- Helper columns to calculate adjusted speed, delivery time, penalty logic

---

## 🧮 Mathematical Model

**Objective Function**:  
Minimize total estimated delivery time  
Minimize ∑ (Xᵢⱼ × tᵢⱼ) + Penalty Time

**Where:**
- `Xᵢⱼ` = 1 if courier j is assigned to order i; 0 otherwise  
- `tᵢⱼ` = estimated delivery time  
- `Penalty Time` = penalty for courier load imbalance

**Constraints:**
- Each order assigned exactly once  
- Couriers must handle at least one order  
- Decision variables must be binary (0/1)  

---

## ⚙️ VBA Automation Highlights

✅ Build assignment and delivery matrices dynamically  
✅ Populate formulas for delivery-time estimates  
✅ Apply Solver settings (objective, constraints) programmatically  
✅ Clear previous runs and reset automatically  
✅ Trigger Outlook email to delivery team with optimized assignments

> 💡 One-click execution for the entire process — scalable, repeatable, and error-free.

---

## 📈 Key Results

| Metric                 | Before       | After        |
|------------------------|--------------|--------------|
| Avg. Delivery Time     | ~40 minutes  | ~33 minutes  |
| Courier Workload       | Unbalanced   | Evenly spread|
| Optimization Time      | Manual setup | Automated via macro |
| Reporting              | Manual emails| Auto-sent via Outlook |

---

## 📂 Files Included

| File Name                         | Description                                      |
|----------------------------------|--------------------------------------------------|
| `Meal_Delivery_Model.xlsx`       | Core optimization model (Solver + Macros)        |
| `Meal_Delivery_Report.docx`      | Full documentation of methods and findings       |
| `Meal_Delivery_Deck.pptx`        | Presentation slides for project walkthrough      |
| `README.md`                      | This file — public-facing project summary        |

---

## 🔮 Future Enhancements

- Migrate to Python + OpenSolver for scale  
- Add delivery **time windows** and **geospatial maps**  
- Integrate with APIs for real-time order ingestion  
- Enable **live ETA tracking** and route optimization logic

---

## 📌 Lessons Learned

- How to frame business problems as optimization models  
- How to automate Excel workflows with logic and code  
- How delivery logistics can be solved with clean data, macros, and Solver

---

> _“This project demonstrated that even complex operational bottlenecks like courier assignments can be solved efficiently using thoughtful modeling, automation, and structured problem-solving — all in Excel.”_
