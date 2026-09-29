🌍 COVID-19 Global Analysis & Short-Term Forecasting

An end-to-end data analysis and forecasting project using reported COVID-19 case data from January–July 2020.

The project combines data cleaning, exploratory data analysis, visualization, descriptive epidemiological indicators, geographic analysis, and time-series forecasting in one reproducible workflow.

📌 Project Highlights

Cleaned and validated 49,068 raw observations.

Aggregated province/state records into consistent country-date observations.

Derived daily confirmed cases, deaths, and recoveries from cumulative totals.

Investigated reporting revisions instead of silently replacing negative daily changes.

Analyzed global trends and 7-day rolling averages.

Compared countries at the final observed date.

Compared trends across WHO regions.

Built an interactive animated world map using Plotly.

Calculated descriptive reported recovery and death ratios.

Built a 14-day time-ordered holdout forecast using Prophet.

Compared the forecast against a naive baseline using MAE and RMSE.

Important: This project analyzes reported surveillance data. It does not estimate the true number of infections and should not be interpreted as a clinical or epidemiological assessment.

🧠 Analytical Questions

How did reported confirmed cases, deaths, and recoveries change globally?

Which countries had the highest cumulative reported cases at the end of the observed period?

How did reported case trajectories differ across WHO regions?

How do reported recovery and death ratios change over time?

What does a 7-day rolling average reveal about daily reporting patterns?

How well can a short-term forecasting model reproduce the final 14 observed days of the cumulative case series?

🛠️ Tech Stack

Python

Pandas — data cleaning, aggregation and transformation

NumPy — numerical calculations

Matplotlib — static visualization

Seaborn — statistical visualization

Plotly — interactive charts and geographic visualization

Scikit-learn — forecasting evaluation metrics

Prophet — time-series forecasting

Jupyter Notebook / Google Colab

📊 Dataset

The dataset contains country-level and province/state-level reported COVID-19 observations with fields including:

Column

Description

Province/State

Province/state where available

Country/Region

Country or territory

Lat, Long

Geographic coordinates

Date

Reporting date

Confirmed

Cumulative reported confirmed cases

Deaths

Cumulative reported deaths

Recovered

Cumulative reported recoveries

Active

Reported active cases

WHO Region

WHO geographic region

The notebook originally used a Google Drive-hosted CSV. For a clean GitHub repository, place the CSV at:

data/covid_19.csv

The notebook will automatically use the local file when it exists; otherwise it falls back to the original URL.

🔄 Project Workflow

Raw Data
   ↓
Data Inspection
   ↓
Data Cleaning & Validation
   ↓
Country-Date Aggregation
   ↓
Daily Change Calculation
   ↓
Global EDA
   ↓
Country & WHO Region Analysis
   ↓
Epidemiological Indicators
   ↓
Rolling Averages
   ↓
Geographic Visualization
   ↓
Time-Series Forecasting
   ↓
Model Evaluation
   ↓
Findings & Limitations

🔍 Key Analysis Areas

Global Trends

Cumulative and daily reported confirmed cases, deaths, and recoveries are visualized over time.

Country Comparison

Countries are compared using the latest date available in the dataset rather than mixing observations from different dates.

WHO Region Analysis

Country-level observations are aggregated by WHO region to examine broader regional trajectories.

Rolling Average

A 7-day rolling average is used to reduce short-term reporting noise and make the underlying trend easier to inspect.

Reported Recovery & Death Ratios

The project calculates:

Reported death ratio = cumulative deaths / cumulative confirmed cases
Reported recovery ratio = cumulative recovered / cumulative confirmed cases

These are descriptive ratios within the dataset and should not be interpreted as individual probabilities or clinical rates.

🔮 Forecasting Methodology

The forecasting section uses Prophet to predict global cumulative confirmed cases.

Instead of training on the entire dataset and forecasting blindly, the final 14 observed days are held out as a test set.

Historical data
───────────────────────────────┬──────────
          Training             │   Test
                               │ 14 days

The model is evaluated using:

MAE — Mean Absolute Error

RMSE — Root Mean Squared Error

A naive baseline that repeats the final training value is included for comparison.

This makes the forecasting section an evaluated modelling exercise rather than simply generating a forecast chart.

⚠️ Data Quality Decisions

One important issue in cumulative reporting data is that daily changes can occasionally be negative because of retrospective corrections.

Instead of doing this:

series.clip(lower=0)

the project retains the original reported values and explicitly identifies negative revisions.

This prevents the cleaning process from silently changing the source data.

📁 Repository Structure

COVID-19-Global-Analysis/
│
├── COVID-19_Global_Analysis_Portfolio.ipynb
├── README.md
│
└── data/
    └── covid_19.csv

🚀 How to Run

1. Clone the repository

git clone <your-repository-url>
cd COVID-19-Global-Analysis

2. Install dependencies

pip install pandas numpy matplotlib seaborn plotly scikit-learn prophet jupyter

3. Add the dataset

Place the CSV file at:

data/covid_19.csv

If the local file is not present, the notebook attempts to load the original dataset URL.

4. Run the notebook

jupyter notebook COVID-19_Global_Analysis_Portfolio.ipynb

The notebook can also be opened directly in Google Colab.

📈 Skills Demonstrated

Data cleaning and validation

Pandas groupby and aggregation

Time-series transformation

Feature creation

Exploratory Data Analysis

Data visualization

Interactive Plotly dashboards/charts

Geographic visualization

Rolling averages

Time-series train/test splitting

Forecasting with Prophet

Model evaluation

Data-quality reasoning

Communicating analytical limitations

⚠️ Limitations

The data represents reported cases rather than the true number of infections.

Testing and reporting practices varied between countries.

Retrospective corrections can produce negative daily changes.

Recovery definitions may differ across locations.

The dataset ends in July 2020.

Forecast performance is evaluated on one historical 14-day holdout window and should not be generalized to future outbreaks.

The forecasting target is cumulative confirmed cases, not daily infection incidence.

👤 Author

Ayush
Aspiring Data Scientist

Python · SQL · Data Analysis · Data Visualization · Machine Learning

⭐ This project is part of my Data Science / Data- Analysis portfolio and will continue to evolve as I build more projects.
