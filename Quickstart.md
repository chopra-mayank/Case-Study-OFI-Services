# 🚀 Quick Start Guide: NexGen Logistics Control Tower

Welcome! This guide gets you up and running with the dashboard in **under 5 minutes**.

## 1. Prerequisites (What You Need)

* **Python:** Version 3.9 or higher installed. (Check with `python --version` or `python3 --version` in your terminal).
* **Data Files:** All 7 required CSV files (`orders.csv`, `delivery_performance.csv`, `cost_breakdown.csv`, `routes_distance.csv`, `customer_feedback.csv`, `vehicle_fleet.csv`, `warehouse_inventory.csv`) downloaded.
* **Project Files:** The `app.py` script and `requirements.txt` file downloaded from this repository.

## 2. Setup (Get Ready)

1.  **Create a Project Folder:** Make a new, empty folder on your computer (e.g., `NexGen_Dashboard`).
2.  **Place Files Inside:**
    * Copy `app.py` into this folder.
    * Copy `requirements.txt` into this folder.
    * **Important:** Copy **all 7 CSV data files** directly into this *same* folder. Do **not** put them in a subfolder.
3.  **Open Your Terminal / Command Prompt:**
    * Navigate *into* your project folder using the `cd` command (e.g., `cd path/to/NexGen_Dashboard`).

## 3. Installation (Install Libraries) 

1.  **Create Virtual Environment** (Keeps project libraries separate):
    ```bash
    python -m venv venv
    ```
2.  **Activate Environment:**
    * **macOS / Linux:** `source venv/bin/activate`
    * **Windows (CMD):** `venv\Scripts\activate`
    * **Windows (PowerShell):** `.env\Scripts\Activate.ps1`
    *(Your terminal prompt should now show `(venv)` at the beginning).*
3.  **Install Dependencies:**
    ```bash
    pip install -r requirements.txt
    ```
    *(This downloads Streamlit, Pandas, Plotly, etc. Wait for it to complete.)*

## 4. Launch (Run the App!)

* From your terminal (make sure you're *inside* the project folder and `(venv)` is active):
    ```bash
    streamlit run app.py
    ```

## 5. Explore

* Your web browser should open automatically to the dashboard. If not, copy the **Local URL** from the terminal (usually `http://localhost:8501`) and paste it into your browser.
* **Get Started:**
    1.  **Filters (Left Sidebar):** Try changing the **Date Range** or deselecting a **Carrier**. Notice how the charts and KPIs update instantly.
    2.  **KPIs (Top):** Quickly see the main metrics like Total Profit, Emissions, and Customer Satisfaction for your filtered view.
    3.  **Tabs (Main Area):** Click through `📊 Strategic Quadrant`, `📦 Profitability Deep-Dive`, `⭐ Service Excellence`, `🚚 Fleet Intelligence` (if available), and `📋 Data Explorer`.
    4.  **AI Insights (In Each Tab):** Read the "🧠 Actionable Insights" box. These insights change based on the data shown!
    5.  **Chart Interaction:** Hover over points/bars on charts for details. Click legend items to hide/show data.
    6.  **Export Data:** Go to the `📋 Data Explorer` tab, click "Generate Excel File...", wait, then click "Download Generated Excel File".

## 💡 Pro Tips for Analysis

* **Start Broad, Then Narrow:** Look at the overall picture first, then use filters to investigate specific segments, carriers, or time periods.
* **Use the What-If Slider:** See how potential carbon taxes impact your bottom line. Great for risk assessment.
* **Connect the Dots:** Insights from different tabs tell a story (e.g., Low carrier profit margin in Tab 2 + High delays for that carrier in Tab 3 = Action needed!).
* **Check Fleet Impact:** High overall CO₂? Check Tab 4 – is an aging fleet contributing significantly?

## 🚨 Troubleshooting Common Issues

* **`FileNotFoundError`:** Ensure **all 7 CSVs** are directly in the **same folder** as `app.py` and filenames match exactly.
* **Slow Performance:** Filter by a smaller **Date Range** if you have very large datasets.
* **"No data matches filters"**: Your filters are too restrictive. Widen them (e.g., select all Carriers).
* **Text/Charts Look Wrong:** Hard refresh your browser (Ctrl+Shift+R or Cmd+Shift+R).

---