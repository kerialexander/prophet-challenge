# MercadoLibre Search Traffic and Stock Analysis
Module 8 Prophet Challenge

## Extended Overview

MercadoLibre, the leading e-commerce platform in Latin America, serves over 200 million users and facilitates millions of transactions annually. Understanding user interest and its correlation with financial performance is critical for strategic decision-making and market positioning. This project aims to explore Google search traffic data for MercadoLibre, investigating its relationship with stock price movements and using advanced forecasting methods to predict future trends. 

This comprehensive analysis combines data exploration, seasonality analysis, feature engineering, and predictive modeling to uncover actionable insights. By leveraging **Python** and libraries like `pandas`, `numpy`, `matplotlib`, and `Prophet`, this project illustrates how search traffic data can serve as a proxy for market sentiment and business activity.

### Key Objectives

1. **Detect Unusual Search Traffic Patterns:** Identify spikes or anomalies in Google search traffic data and relate them to significant financial or corporate events.
2. **Analyze Seasonal Trends:** Understand how user interest varies by time of day, day of the week, and season to inform targeted marketing strategies.
3. **Correlate Search Traffic with Stock Performance:** Investigate potential predictive relationships between search interest and stock price movements.
4. **Forecast Future Trends:** Use Prophet to build a time series model that predicts future search traffic, providing insights for operational and strategic planning.

---

## Analysis Details

### Analyzing Unusual Patterns in Search Traffic

- **Data Exploration:** Google search traffic data was loaded and filtered to focus on May 2020, coinciding with the release of MercadoLibre's quarterly financial results. Hourly search data was visualized to identify anomalies.
- **Aggregate Analysis:** The total search traffic for May 2020 was calculated and compared to the monthly median across all months to determine if search interest increased during the financial results period.

### Results Summary:

- Total search traffic during May 2020 exceeded the monthly median by a significant margin.
- Hourly spikes aligned closely with financial reporting dates, indicating potential investor interest.

![Search Traffic Visualization](search_traffic_chart.png)

---

### Seasonal Trends in Search Traffic

- **Hourly Patterns:** Search traffic data was grouped by hour to calculate and plot average traffic throughout the day. This revealed the times of day with peak activity.
- **Daily Patterns:** Average traffic by day of the week was computed and visualized, highlighting specific days with higher engagement.
- **Weekly Trends:** Data was grouped by week of the year to identify seasonal increases, particularly during the winter holiday period.

### Results Summary:

- **Peak Hours:** The highest traffic occurred between **8 PM and 12 AM**, indicating that users are most active during late evening hours.
- **Least Traffic Hours:** The lowest activity was observed between **2 AM and 6 AM**.
- **Busiest Days:** Traffic peaked on **Wednesdays and Thursdays**, reflecting mid-week engagement.
- **Lowest Traffic Days:** Sundays consistently showed reduced search traffic.
- **Seasonal Peaks:** Significant increases in search activity occurred during **weeks 48 to 52**, aligning with the holiday shopping season.

---

### Relating Search Traffic to Stock Price Patterns

- **Data Integration:** Stock price data was merged with search traffic data for analysis, focusing on the first half of 2020 to capture the impact of market events.
- **Trend Comparison:** Search traffic and stock prices were plotted together to identify correlations.
- **Feature Engineering:** New features, including lagged search trends, stock volatility (4-hour rolling average), and hourly stock returns, were created to explore relationships between search behavior and stock performance.

### Results Summary:

- Positive correlations were observed between increased search traffic and stock price volatility.
- Lagged search trends indicated that spikes in search interest often preceded stock price movements, suggesting predictive value in search data.

---

### Time Series Forecasting with Prophet

- **Model Training:** Google search traffic data was prepared for Prophet, with columns `ds` (datetime) and `y` (search traffic). The model was trained to predict future trends.
- **Forecast Visualization:** The forecasted search trends were plotted, providing a near-term outlook for MercadoLibre's popularity.
- **Component Analysis:** Time series components (daily, weekly, yearly) were visualized, revealing:
  - **Peak Times:** Search traffic was highest during late evenings.
  - **Busiest Days:** Wednesdays and Thursdays consistently showed higher search interest.
  - **Lowest Activity:** Reduced search traffic occurred on Sundays and during the early morning hours (2 AM to 6 AM).

### Results Summary:

- The forecast predicted stable growth in search traffic, with notable seasonal peaks during the holiday period.
- Daily and weekly trends provided actionable insights for marketing and operational planning.

---

## File Structure

```
prophet-challenge/
├── data/
│   ├── search_data.csv
│   ├── stock_price_data.csv
├── notebooks/
│   ├── mercado_analysis.ipynb
├── README.md
├── search_traffic_chart.png
└── requirements.txt
```

---

## Requirements

- **Python** 3.8+
- Libraries:
  - `pandas`
  - `numpy`
  - `matplotlib`
  - `Prophet`

Install dependencies using the following command:

```bash
pip install -r requirements.txt
```

---

## Deliverables

1. Jupyter Notebook (`mercado_analysis.ipynb`) with:
   - All analysis steps implemented.
   - Visualizations and insights.
2. Written responses to the questions in the starter file.

---

## Goals and Outcomes

- Highlight correlations between search traffic and financial events.
- Uncover seasonal trends in user interest.
- Identify predictive relationships between search traffic and stock performance.
- Use time series modeling to forecast future search traffic trends.

---

## Support

For any questions or issues, please contact:

- Keri Alexander
- Email: [Keri Alexander](keri.m.alexander@gmail.com)

---

## Acknowledgments

Special thanks to MercadoLibre for providing inspiration for this analysis and to the creators of Prophet for their powerful time series forecasting tool.
