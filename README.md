# 🇨🇭 Swiss-Energy-Analytics Project - Built with ❤️ by Soubhi SAAD

A full-stack data science project analyzing Switzerland’s electricity landscape in 2024 — combining real energy data, interactive dashboards, statistical summaries, and machine learning predictions.

Data sourced from **Swissgrid** : https://www.swissgrid.ch/en/home.html

**🔍 Objectives**
- Track monthly energy consumption vs production
- Analyze regional (canton-level) energy autonomy
- Visualize net energy balances and import/export patterns
- Predict energy usage with Random Forest and XGBoost
- Communicate insights using Power BI dashboards

**🛠️ Tools & Technologies**
- Python (Pandas, Matplotlib, Seaborn)	-> Data cleaning & visualization
- Power BI	-> DAX + Interactive reporting
- Excel	-> Swissgrid dataset format .xlsx initial data exploration
- VS Code	Development IDE
- Scikit-learn, XGBoost	Machine learning


Note: The public dataset can be found in this repository. Each day's data is recorded at 15-minute intervals, which means:

There are 96 records per day (24 hours × 4 intervals per hour) the unit is in kWh.

This high-resolution data allows for:
- Detailed time series analysis
- Accurate short-term forecasting
- Peak load detection and consumption trends

To simplify modeling and visualization, some analyses aggregate the data to hourly or daily totals, while others retain the 15-minute granularity to capture finer energy usage patterns.

**📈 Python Analysis Highlights**

Monthly Energy Trends
- Total annual consumption: 61,63 TWh
- Daily average: 167.92 GWh
- Consumption peaks in winter (Jan, Dec) and dips in summer (Jun–Aug)

Production vs. Consumption
- Production significantly exceeds consumption in summer (Jul–Aug).
- Winter months show a shortfall, with consumption surpassing production.

Net Energy Balance : Surplus in summer (hydropower peak), deficit in December.

Imports and Exports
 - Summer: Switzerland exports electricity (mostly hydropower).
 - Winter: Imports spike, especially in December


**📊 Power BI Dashboard Insights**
National Overview & Metric	Value
- Total Produced	75.57 TWh
- Total Consumed	61.63 TWh
- Net Balance	+13.94 TWh

⚠️ Although annual production exceeds consumption, seasonal variations cause import dependence in winter.


![image alt](https://github.com/soubhisaad/Swiss-Energy-Analytics-Project-Soubhi-Saad/blob/24a5466d12b0809f04eb2fb3e94a345ac2df36f8/Power%20BI%20Dashboard.png)


**Canton-Level Production vs. Consumption**
 - Cantons like Aargau (AG) and Valais (VS) produce more than they consume.
 - Others like Zurich (ZH) and Geneva (GE) consume far more than they produce.

**🌍 Foreign Trade Overview**
- Imported energy: 25.26 TWh
- Exported energy: 39.18 TWh
- Net foreign balance: –13.92 GWh

Switzerland was a net exporter of electricity, exporting 13.92 TWh more than it imported.

**Key Insights**
Switzerland is energy-exporting in summer (hydropower surplus).
❄️ Switzerland becomes energy-importing in winter due to heating demand and lower renewable output.
📊 The country is not fully energy-autonomous year-round, despite strong seasonal performance.

_"Cela confirme que la Suisse n’est pas totalement autosuffisante en électricité sur l’année, même si elle produit beaucoup à certains moments."_



**Energy Machine Learning Models**
- Random Forest (RF)
- XGBoost (XGB)

Models trained to predict hourly energy consumption totals

⚙️ Feature Engineering
- Lag features: lag_1h, lag_24h
- Time features: hour, day of week, is_weekend
- Rolling means: roll_6h, roll_24h
- Grid data: grid_feed_in, net_outflow

**📊 Prediction Performance**
- XGBoost better on volatile 15-min targets
- Random Forest (RF) excels on aggregated hourly predictions


![image alt](https://github.com/soubhisaad/Swiss-Energy-Analytics-Project-Soubhi-Saad/blob/776207e4d887028048621bc525cc5c067287bb1c/Prediction%20accuracy%20of%20RF%20and%20XGBoost.png)

Note: To continue this project, we could incorporate models like ARIMA or Prophet (from Meta) to enhance the predictive capabilities for future energy consumption trends.












