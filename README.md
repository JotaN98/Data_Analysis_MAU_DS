# Green Energy Transition & Economic Growth

**Authors:** Peter Gustafson & João Domingos  
**Course:** Data and Society
**Institution:** Malmö University, Dept. of Computer Science and Media Technology  
**Date:** January 2026  

## 📌 Project Overview
This project investigates the relationship between a country's economic size (GDP) and its transition to renewable energy. By analyzing global data from 1990 to 2022, this study tests the validity of the **Renewable Kuznets Curve (RKC)**—the hypothesis that renewable energy adoption follows a U-shaped relationship with economic development.

The analysis focuses on three key indicators:
1.  **Renewable Electricity Production (Absolute TWh):** Does total green energy output increase with GDP?
2.  **Renewable Energy Share (%):** Does the *proportion* of green energy in the total mix increase with GDP?
3.  **$CO_{2}$ Emissions:** Do emissions eventually decrease at high income levels?

## 📊 Key Findings
Based on the pooled analytics performed in this study:
* **Production:** Renewable energy production increases with economic size, accelerating significantly at higher GDP levels (Quadratic fit, $R^2 = 0.431$).
* **Share:** The *share* of renewables initially declines as developing economies rely on fossil fuels. It only begins to rise again at very high income levels, confirming a U-shaped relationship.
* **Emissions:** $CO_{2}$ emissions rise steadily with GDP, with a potential downturn observed only in the highest-income economies.

## 📂 Repository Structure
* `datasociety_finalproject.ipynb`: The main Jupyter Notebook containing data extraction, processing, statistical modeling (OLS), and visualization code.
* `Data & Society - Final Project.pdf`: The final academic report detailing the motivation, literature review, and discussion of results.
* `README.md`: Project documentation.

## 🛠️ Data Sources
This project utilizes dynamic data fetching (no local CSVs required) from the following sources:
* **World Bank (via API):** GDP (current USD) and Renewable Energy Consumption (% of total).
* **Our World in Data (OWID) & Ember:** Renewable electricity generation (TWh) and $CO_{2}$ emissions.

## 💻 Tech Stack & Dependencies
The analysis is written in **Python**. You will need the following libraries installed:

* `pandas` (Data manipulation)
* `numpy` (Numerical operations)
* `matplotlib` (Visualization)
* `statsmodels` (Statistical regression/OLS)
* `wbgapi` (World Bank API wrapper)

## 🚀 Installation & Usage

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/yourusername/green-energy-transition.git](https://github.com/yourusername/green-energy-transition.git)
    cd green-energy-transition
    ```

2.  **Install dependencies:**
    It is recommended to use a virtual environment.
    ```bash
    pip install pandas numpy matplotlib statsmodels wbgapi
    ```

3.  **Run the Analysis:**
    Open the Jupyter Notebook and run all cells.
    ```bash
    jupyter notebook datasociety_finalproject_260113.ipynb
    ```
    *Note: The notebook fetches data directly from remote URLs and APIs. An active internet connection is required.*

## 📈 Methodology
The code performs the following steps:
1.  **Data Ingestion:** Fetches live data from OWID GitHub repositories and the World Bank API.
2.  **Preprocessing:** Merges datasets on ISO3 country codes and Year. Handles missing values and performs Logarithmic transformations (`log` and `log1p`) to normalize skewed economic data.
3.  **Statistical Modeling:** Applies Ordinary Least Squares (OLS) regression to test quadratic models ($y = \beta_0 + \beta_1 x + \beta_2 x^2$).
4.  **Visualization:** Generates scatter plots with quadratic trendlines to visualize the turning points of the transition.

## ⚖️ License & Ethics
This project includes an ethical reflection on the environmental impact of manufacturing renewable systems and the classification of biomass as a renewable source.

**Citation:**
Gustafson, P., & Domingos, J. (2026). *Green Energy Transition: Does Economic Growth Drive Transition to Renewable Energy?* Malmö University.
