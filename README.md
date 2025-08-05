## 📈 Time Series Visualization & Feature Engineering in Python
---

This project demonstrates a complete workflow for visualizing and analyzing time series data using Python. It covers daily sales data over a 6-month period and includes all key techniques for trend, seasonality, smoothing, and feature engineering.

---

### 🗃 Dataset

- **Synthetic sales data**
- 180 daily records
- Columns: `Date`, `Sales`

---

### 🧰 Libraries Used

- `pandas`
- `numpy`
- `matplotlib`
- `seaborn`
- `plotly.express`
- `statsmodels`

---

### 🔍 Key Concepts & Visualizations

#### ✅ 1. Basic Line Plot (Matplotlib)
Shows the overall shape and fluctuations of the daily time series.

#### ✅ 2. Rolling Averages
```python
df["Sales_7D_Avg"] = df["Sales"].rolling(window=7).mean()
Smooths short-term noise to reveal trends.
```

#### ✅ 3. Seaborn Boxplot
Visualizes seasonal distribution patterns (e.g., weekday effects).

#### ✅ 4. ACF & PACF (Statsmodels)
Autocorrelation and partial autocorrelation help identify temporal dependencies.

#### ✅ 5. Time Series Decomposition
```python
seasonal_decompose(df["Sales"], model="additive", period=30)
Breaks the series into trend, seasonality, and residual.
```

#### 📊 Techniques Demonstrated
| Technique            | Tool/Function                          |
| -------------------- | -------------------------------------- |
| Line Plot            | `matplotlib.pyplot.plot()`             |
| Rolling Mean         | `pandas.rolling()`                     |
| Seasonality Analysis | `seaborn.boxplot()`                    |
| Interactive Chart    | `plotly.express.line()`                |
| ACF/PACF Analysis    | `statsmodels.graphics.tsaplots`        |
| Decomposition        | `statsmodels.tsa.seasonal_decompose()` |
| Time Indexing        | `df.set_index("Date")`                 |
| Resampling           | `df.resample("M").mean()`              |
| Lag Features         | `df.shift(1), df.diff()`               |
