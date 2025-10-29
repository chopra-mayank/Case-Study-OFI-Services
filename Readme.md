# NexGen Logistics Control Tower

## 📘 Table of Contents
1. [Problem Statement](#1-problem-statement-the-logistics-trilemma)
2. [Our Solution](#2-our-solution-the-logistics-control-tower)
3. [Key Features](#3-key-features)
4. [Project Structure](#4-project-structure-)
5. [Setup & Usage](#5-setup--usage-running-on-localhost)
6. [How It Works](#6-how-it-works-️)
7. [Technical Stack & KPIs](#7-technical-stack--kpis)
8. [Data Requirements](#8-data-requirements)
9. [Troubleshooting](#9-troubleshooting)
    
---

## 1. Problem Statement: The Logistics Trilemma

Modern logistics operates under the pressure of optimizing three often conflicting goals: maximizing **Profitability**, ensuring **Sustainability**, and delivering excellent **Performance**. Traditional tools analyze these in silos, creating critical blind spots:

* **Hidden Costs:** Profit calculations ignore warehouse storage costs, misrepresenting true **end-to-end profitability**.  
* **Disconnected Sustainability:** Aggregate CO₂ data isn't linked to **per-order profitability** or **fleet health**.  
* **Opaque Performance Issues:** Customer feedback isn’t tied back to specific **carriers, routes, or operational failures**.

The result: suboptimal trade-offs — the **“Logistics Trilemma.”**

---

## 2. Our Solution: The Logistics Control Tower

The **Logistics Control Tower** is an interactive Streamlit dashboard built with Python (Pandas + Plotly) that unifies **all seven NexGen datasets** into a single, integrated view.

**Key Innovations**
* True **End-to-End Profitability** (`E2E_Profit_INR`)
* **Profit vs. Sustainability Quadrant** analysis  
* **Carbon Tax Simulator** (₹0–₹50/kg CO₂)  
* **AI-Generated Actionable Insights**  
* **Advanced Visualizations:** Treemaps, Sunbursts, Gauges, Heatmaps  
* **Modern UI/UX:** Clean, professional, and responsive  

This dashboard empowers managers and analysts to optimize all three pillars — **profitability**, **sustainability**, and **service quality** — simultaneously.

---

## 3. Key Features

* **Holistic Data Integration**: Combines all 7 CSVs (`orders`, `delivery_performance`, `cost_breakdown`, `routes_distance`, `customer_feedback`, `warehouse_inventory`, `vehicle_fleet`).
* **Strategic Quadrant Analysis**: Classifies orders into 'Best-in-Class', 'Optimize for Green', 'Scale Up', and 'Critical Intervention' based on profit and CO₂.
* **Profitability Deep Dive**: Violin plots, Treemaps, and Carrier margin comparisons.
* **Service Excellence Dashboard**: Reliability heatmaps, delivery speed analysis, and customer sentiment mapping.
* **Fleet Intelligence Module**: Health gauges, scatter plots, and fleet composition charts.
* **Dynamic AI Insights**: Context-aware recommendations based on filtered data.
* **What-If Carbon Tax Simulation**: Adjust profit dynamically with an interactive slider.
* **Data Explorer & Export**: Preview and download filtered data as `.xlsx`.

---

## 4. Project Structure 📁

```text
NexGen_Logistics_Control_Tower/
│
├── app.py                  # Main Streamlit application
├── requirements.txt        # Python dependencies
├── README.md               # This file
├── Innovation_Brief.pdf    # Business case & technical report
│
├── cost_breakdown.csv      # REQUIRED: All 7 data files in this folder
├── customer_feedback.csv
├── delivery_performance.csv
├── orders.csv
├── routes_distance.csv
├── vehicle_fleet.csv
└── warehouse_inventory.csv
```

---

## 5. Setup & Usage (Running on localhost)

**Prerequisites:**
* Python 3.9+ installed
* All 7 CSVs placed in the same directory as `app.py`

**Steps:**

```bash
# 1. Create and enter project folder
mkdir NexGen_Logistics_Control_Tower && cd NexGen_Logistics_Control_Tower

# 2. Clone repo or add files
# git clone https://github.com/<your-username>/NexGen-Logistics-Control-Tower.git

# 3. Create a virtual environment
python -m venv venv

# 4. Activate it
# macOS / Linux
source venv/bin/activate
# Windows
venv\Scripts\activate

# 5. Install dependencies
pip install -r requirements.txt

# 6. Run the Streamlit app
streamlit run app.py
```

Access the dashboard at: **http://localhost:8501**

---

## 6. How It Works

* **Tabs**: Navigate between strategic, profitability, service, and fleet views.  
* **Sidebar Filters**: Adjust by Date, Carrier, Segment, and more.  
* **Interactivity**: Hover, zoom, or filter within Plotly charts.  
* **AI Insights**: Get real-time, context-based recommendations.  
* **Data Explorer**: Download filtered data snapshots for offline analysis.

---

## 7. Technical Stack & KPIs

**Core Stack**: Python 3.9+, Streamlit, Pandas, NumPy, Plotly  
**Styling**: Custom CSS for professional UI  
**Key KPIs**:
* `E2E_Profit_INR`, `Adjusted_Profit_INR`
* `Total_CO2_kg`, `CO2_per_KM`
* `Carrier_Performance_Score`, `Cost_per_KM`

---

## 8. Data Requirements

Seven CSV files required in the project root:

1. `orders.csv`
2. `delivery_performance.csv`
3. `cost_breakdown.csv`
4. `routes_distance.csv`
5. `customer_feedback.csv`
6. `vehicle_fleet.csv`
7. `warehouse_inventory.csv`

Refer to **Mayank_Chopra.pdf** for detailed schema.

---

## 9. Troubleshooting 

* **FileNotFoundError** → Ensure all CSVs are in the same folder as `app.py`  
* **ModuleNotFoundError** → Run `pip install -r requirements.txt`  
* **No Data** → Loosen sidebar filters  
* **Slow Load** → Use smaller date ranges or restart app (`Ctrl+C`, then rerun)  
* **Chart Display Issues** → Hard refresh your browser

---
