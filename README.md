# Cricket-World-Cup-2023_Analysis

This project analyzes match data from the ICC Cricket World Cup 2023 using Python, Pandas, and Seaborn. The analysis includes statistical summaries, data visualizations, and exploration of trends related to match outcomes, team performance, and other key metrics.

---

## 📁 Dataset

- **File:** `CWC2023.csv`
- **Total Matches:** 48
- **Columns:** 14
- **Features include:**
  - Match Number
  - Team 1 and Team 2
  - Venue, Toss, and Choice
  - Innings runs, balls, and wickets
  - Match winner and margin of victory

---

## 🧠 Analysis Highlights

### ✔️ Data Exploration
- Checked data types and structure using `df.info()`
- Verified absence of missing values using `df.isnull().sum()`
- Filtered data based on conditions (e.g., matches with number > 25)

### 📊 Descriptive Statistics
- Computed `mean`, `median`, and `standard deviation` for key columns like:
  - Innings1_Wickets
  - Innings1_Run, Innings2_Run
  - Innings1_Balls, Innings2_Balls

### 📈 Visualizations

1. **Scatter Plot**
   - Relationship between `Match_No` and `Innings1_Wickets` for early matches

2. **Correlation Heatmap**
   - Used `Seaborn` to visualize correlation between numeric features

3. **Histogram**
   - Distribution of match numbers using `sns.histplot`

---

## 🔍 Data Cleaning

- Handled missing values with:
  ```python
  df_filled = df.fillna(df.mean())
````

* Removed duplicate rows:

  ```python
  df_no_duplicates = df_filled.drop_duplicates()
  ```

---

## 🛠️ Technologies Used

* Python 3.x
* Pandas
* Matplotlib
* Seaborn
* Google Colab / Jupyter Notebook

---

## 🧾 Sample Code Snippets

```python
# Read dataset
import pandas as pd
df = pd.read_csv("CWC2023.csv")

# Basic stats
mean_values = df.mean()
print(mean_values)

# Visualize correlation
import seaborn as sns
import matplotlib.pyplot as plt
sns.heatmap(df.corr(), annot=True, cmap='coolwarm')
```

---

## 📌 Suggested Folder Structure

```
icc-cwc2023-analysis/
├── CWC2023.csv
├── cwc2023_analysis.ipynb
├── README.md
└── plots/
    ├── heatmap.png
    ├── scatterplot.png
    └── histogram.png
```

---

## 📊 Insights & Observations

* Most matches had between 7–10 wickets in the first innings.
* Average score in Innings 1 was around 289 runs.
* Teams batting second won frequently when chasing scores < 260.
* India and Australia had standout performances in terms of win margins.

---

## 🙋‍♂️ Author

**D. Lalith Kumar**
B.Tech CSE (AI & ML)

---

## 📜 License

This project is intended for academic and educational purposes. Feel free to use, modify, and cite appropriately.
