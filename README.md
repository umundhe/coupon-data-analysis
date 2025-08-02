
# Coupon Acceptance Prediction

## Assignment Overview

This project explores customer behavior in response to digital coupons delivered during driving scenarios. The main objective is to analyze and predict **whether a driver will accept a coupon**, based on features like destination, time, weather, passenger type, and more.

The data comes from the [UCI Machine Learning Repository](https://archive.ics.uci.edu/), collected through a Mechanical Turk survey that simulated various driving scenarios.

---

##  Dataset Description

- **Source**: UCI ML Repository – Coupon Dataset
- **Target variable**: `Y`  
  - `1` = Customer accepted the coupon  
  - `0` = Customer rejected the coupon
- **Coupon Types**:
  - Restaurant (under $20)
  - Coffee House
  - Carry out & Take away
  - Bar
  - Restaurant ($20–$50)

---

##  What This Notebook Does

### Data Preprocessing
- Handles missing values:
  - Drops `car` column (99% missing)
  - Imputes mode for `Bar`, `CoffeeHouse`, `CarryAway`, and `RestaurantLessThan20`
- Converts `age` into numeric form

### Visualizations
- Histograms and heatmaps showing:
  - Coupon acceptance by temperature
  - Gender × Age
  - Occupation × Income

### Modeling
- Logistic regression models for:
  - Bar coupons
  - Coffee House
  - Restaurant (<$20)
- Evaluation of feature impact and model performance

---

##  Requirements

```bash
pip install pandas numpy matplotlib seaborn scikit-learn
```

---

##  File Structure

- `prompt.ipynb`: Main notebook for analysis and modeling
- `data/coupons.csv`: Dataset file 
- `README.md`: Project overview and documentation

---

##  Summary of Findings

- Younger, lower-income drivers are more likely to accept coupons.
- Acceptance varies significantly by **coupon type**, **passenger**, and **occupation**.
- Logistic models show moderate accuracy (65–73%) depending on coupon type.

---

## Next Steps

- Explore non-linear models (e.g., Random Forest, XGBoost)
- Add spatial/time-based features (e.g., time of day, trip duration)
- Deploy as an interactive dashboard

---

##  Author

*This notebook was developed as part of an educational assignment in data visualization and modeling.*
