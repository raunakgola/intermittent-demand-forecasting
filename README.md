---

# 📦 Intermittent Demand Forecasting with Croston’s Method

## 📘 Project Overview

This project focuses on forecasting intermittent demand patterns using Croston’s method. Intermittent demand refers to situations where products are not sold regularly—there are many periods with no sales, making it hard for traditional forecasting methods to predict future demand accurately. Croston’s method addresses this by separately modeling demand sizes and intervals, providing more accurate forecasts for such data.

## 🎯 Objectives

* **Implement Croston’s Method**: Develop a Python-based implementation of Croston's method to forecast intermittent demand.

* **Evaluate Model Performance**: Assess the model using metrics like MAE, RMSE, sMAPE, and MASE.

* **Visualize Forecasts**: Create visual representations to compare actual and forecasted demand values.

* **Document Insights**: Compile findings and insights into a comprehensive report.

## 🧠 Learning Outcomes

Through this project, we have:

* **Understood Intermittent Demand**: Gained insights into the challenges of forecasting intermittent demand and the limitations of traditional models.

* **Mastered Croston’s Method**: Learned the theoretical underpinnings and practical implementation of Croston's method.

* **Enhanced Data Handling Skills**: Improved proficiency in data preprocessing, time series analysis, and visualization using Python libraries.

* **Developed Evaluation Techniques**: Acquired skills in evaluating model performance using appropriate metrics for intermittent demand scenarios.

## 🛠️ Methodology

1. **Data Preparation**: Loaded and preprocessed the dataset, focusing on a specific SKU to analyze daily demand patterns.

2. **Model Implementation**: Implemented Croston's method, which involves:

   * Identifying non-zero demand occurrences.

   * Calculating the average demand size and average interval between demands.

   * Applying exponential smoothing to both components.

   * Forecasting future demand as the ratio of the smoothed demand size to the smoothed interval.

3. **Rolling Forecast**: Performed a rolling forecast to generate one-step-ahead predictions across the dataset, allowing for a comprehensive evaluation of model performance over time.

4. **Performance Evaluation**: Assessed the model using the following metrics:

   * **MAE (Mean Absolute Error)**: 10.02

   * **RMSE (Root Mean Squared Error)**: 24.28

   * **sMAPE (Symmetric Mean Absolute Percentage Error)**: 178.33%

   * **MASE (Mean Absolute Scaled Error)**: 0.398

5. **Visualization**: Plotted actual vs. forecasted demand to visually assess model accuracy and identify patterns or discrepancies.

## 📈 Results & Insights

* **Model Accuracy**: The low MAE and MASE values indicate that Croston's method provides a reasonable forecast for intermittent demand, outperforming naive models.

* **High sMAPE**: The elevated sMAPE suggests significant relative errors, which is common in intermittent demand scenarios due to the prevalence of zero values.

* **Forecast Stability**: Croston's method produces constant forecasts between non-zero demands, aligning with its design but potentially limiting responsiveness to sudden demand changes.

## 📄 Report

A detailed report summarizing the methodology, findings, and insights is available in the `report.pdf` file. This document includes:

## 📁 Project Structure

```
├── data/
│   └── online_retail_clean.csv
├── notebooks/
│   └── croston_forecasting.ipynb
├── report/
│   └── report.pdf
├── README.md
└── requirements.txt
```

## 🔧 Installation & Usage

1. **Clone the Repository**:

   ```bash
   git clone https://github.com/raunakgola/intermittent-demand-forecasting.git
   cd intermittent-demand-forecasting
   ```

2. **Create a Virtual Environment**:

   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. **Install Dependencies**:

   ```bash
   pip install -r requirements.txt
   ```

4. **Run the Notebook**:

   Open `croston_forecasting.ipynb` in Jupyter Notebook or JupyterLab and execute the cells sequentially.

## 📚 References

* Croston, J.D. (1972). *Forecasting and Stock Control for Intermittent Demands*. Operational Research Quarterly, 23(3), 289-303.

* [Croston's Method for Intermittent Time Series Forecasting in NumPyro](https://juanitorduz.github.io/croston_numpyro/)

* [Forecasting Intermittent Demand with the Croston Model](https://medium.com/towards-data-science/croston-forecast-model-for-intermittent-demand-360287a17f5f)


