# Dynamic Pricing Strategy (Python)

A data-driven solution that implements **dynamic pricing** for ride-sharing or similar services. By analyzing factors such as demand, supply, and customer behavior, this project demonstrates actionable techniques to adjust prices in real time and maximize revenue and profitability.

---

## 🚀 Project Overview

Dynamic pricing is a modern data science approach that adapts prices based on real-time conditions. This project processes ride-level data (rider volume, driver availability, location category, loyalty, and expected ride duration) to derive pricing strategies. It includes both heuristic rules and an ML-based model to recommend optimized ride costs dynamically.  
This aligns with industry-standard pricing strategies discussed in the Aman XAI article on building dynamic pricing using Python :contentReference[oaicite:2]{index=2}.

---

## 🎯 Objectives

- **Optimize revenue** through real-time price adjustments using demand–supply multipliers.
- **Simulate elastic/inelastic customer segments** via data-driven thresholds.
- **Train a predictive model** (e.g. RandomForestRegressor) to estimate optimal pricing.
- **Visualize pricing impact** and profit margins using Plotly.

---

## ⚙️ Key Features

1. **Data Preprocessing & EDA**  
   Clean, inspect, and segment data; explore relationships via descriptive statistics, scatter plots, box plots, and heatmaps.

2. **Rule‑Based Pricing Logic**  
   - Define demand/supply thresholds (e.g., high vs. low percentiles).
   - Compute multipliers:  
     - `demand_multiplier = actual riders ÷ percentile threshold`  
     - `supply_multiplier = actual drivers ÷ percentile threshold`  
     - Adjust ride cost by combining demand and supply multipliers with fixed caps/floors for stability.

3. **Elasticity‑Based Segmentation**  
   Segment customers into **Low / Medium / High elasticity** groups and apply differential pricing:
   - Raise prices ~5% for inelastic segments
   - Discount ~10% for highly elastic segments :contentReference[oaicite:3]{index=3}

4. **Machine‑Learning Modeling**  
   Train a RandomForestRegressor on historical rides to predict adjusted costs. Visualize predicted vs actual pricing to assess model performance.

5. **Interactive Visualizations**  
   Dynamic charts (scatter, box, donut, and correlation plot) highlighting price distributions, profit margins, and elasticity-by-segment analysis.

---

## 📂 Dataset

| Column                     | Description                                      |
|---------------------------|--------------------------------------------------|
| `Number_of_Riders`        | Ride demand level                                |
| `Number_of_Drivers`       | Supply availability                              |
| `Location_Category`       | Urban / Suburban / Rural                         |
| `Customer_Loyalty_Status` | Loaylty tier (e.g., Silver, Gold, Regular)       |
| `Number_of_Past_Rides`    | Customer experience level                        |
| `Average_Ratings`         | Customer feedback                                |
| `Time_of_Booking`         | Time segment of booking                          |
| `Vehicle_Type`            | Economy, Premium, etc.                           |
| `Expected_Ride_Duration`  | Estimated ride duration in minutes               |
| `Historical_Cost_of_Ride` | Actual cost before dynamic adjustments           |

Ensure the `dynamic_pricing.csv` dataset is placed in the project folder to facilitate notebook execution.

---
## 📈 Insights & Future Enhancements

Dynamic pricing yielded notable revenue uplift via elasticity-based adjustments and demand–supply multipliers.
Profitability trends and discount strategies vary significantly across customer segments.

**Next steps could include:**

- Tuning thresholds via cross-validation or A/B testing
- Using reinforcement learning or multi-armed bandits for real-time optimization  
- Incorporating competitor pricing, seasonal effects, and event-driven surges
- Deploying as a **Streamlit** or **Flask** app for live simulations or dashboards

---

## 📝 Contributing

Contributions are highly welcome:

- Fork the repository  
- Make changes or add features  
- Submit a pull request with your enhancements

---

## 📄 License

This project is licensed under the **MIT License**. See the LICENSE file for details.

---

## 👤 About the Author

**Om Aditya** – Passionate about applying data science to real-world revenue optimization problems.

Feel free to connect or reach out for collaboration or feedback!

