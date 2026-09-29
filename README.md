# Adult Income Dataset – Exploratory Data Analysis

## 📌 Project Overview

This project focuses on **Exploratory Data Analysis (EDA)** and **Data Cleaning** using the Adult Income dataset.

The main objective of this project is to understand the structure of the dataset, perform different data analysis operations, handle missing and inconsistent values, detect outliers, and visualize important patterns using Python.

The project was developed using **Pandas, NumPy, Matplotlib, Seaborn, SciPy, and AutoViz**.

---

## 📊 Dataset

The dataset used in this project is the **Adult Income Dataset**.

It contains information about individuals such as:

* Age
* Workclass
* Education
* Education Number
* Marital Status
* Occupation
* Relationship
* Race
* Sex
* Capital Gain
* Capital Loss
* Hours per Week
* Native Country
* Income

The target variable is **Income**, which contains two categories:

* `<=50K`
* `>50K`

---

## 🎯 Project Objectives

The main objectives of this project are:

1. Understand the structure and characteristics of the dataset.
2. Perform basic data exploration using Pandas.
3. Filter and select relevant records and columns.
4. Calculate descriptive statistics.
5. Analyze categorical variables.
6. Calculate percentages and aggregate values.
7. Identify missing and inconsistent values.
8. Handle missing values using different techniques.
9. Detect and handle outliers.
10. Create meaningful visualizations to understand relationships within the data.

---

## 🛠️ Technologies Used

* **Python**
* **Pandas**
* **NumPy**
* **Matplotlib**
* **Seaborn**
* **SciPy**
* **AutoViz**
* **Jupyter Notebook / Google Colab**

---

## 🔍 Exploratory Data Analysis

The project includes several EDA operations, including:

### Dataset Understanding

* `df.info()`
* `df.describe()`
* `df.head()`
* `df.tail()`
* `df.shape`
* `df.count()`

### Data Filtering

Examples include:

* Finding people above a particular age.
* Filtering people based on income.
* Finding people working more than a specific number of hours.
* Filtering people within a specific age range.
* Selecting specific education categories.

### Statistical Analysis

The project calculates:

* Mean
* Median
* Minimum
* Maximum
* Standard deviation
* Correlation
* Aggregations by income category

### Categorical Analysis

The project also examines:

* Unique education categories
* Unique workclass values
* Number of unique occupations
* Value counts
* Percentage distribution of education and income categories

---

## 🧹 Data Cleaning

The dataset contains inconsistent/missing values represented by `?`.

These values are identified and handled during the cleaning process.

Different approaches explored in the project include:

### Replacing Missing Values

```python
df = df.replace(" ?", None)
```

### Filling Missing Values

Different techniques were explored, including:

* Constant values
* Mean
* Median
* Mode
* Forward fill
* Backward fill
* Interpolation

### Removing Missing Records

```python
df.dropna(inplace=True)
```

Whitespace inconsistencies are also handled using:

```python
df = df.map(lambda x: x.strip() if isinstance(x, str) else x)
```

---

## 📈 Outlier Detection

The project explores different methods for detecting outliers.

### IQR Method

The Interquartile Range (IQR) method is used to identify unusual values in numerical columns.

### Z-Score Method

Z-scores are calculated using SciPy to identify observations that are significantly different from the mean.

### Winsorization

Winsorization is also explored as a technique for limiting extreme values.

These techniques are applied to numerical variables such as:

* Age
* Education Number

---

## 📊 Data Visualizations

Five different charts were created to understand patterns in the dataset.

### 1. Income Count by Education Level

A bar/count chart is used to compare income categories across different education levels.

### 2. Income Distribution

A donut chart shows the proportion of people earning `<=50K` and `>50K`.

### 3. Age vs Hours Worked

A scatter plot is used to examine the relationship between age and hours worked per week, while also distinguishing income categories.

### 4. Education vs Marital Status

A heatmap shows the average number of hours worked per week across education levels and marital-status categories.

### 5. Working Hours Across Age

A line chart shows the average working hours across different age groups for the two income categories.

---

## 🤖 Automated Visualization

The project also explores **AutoViz** for automatically generating visualizations from the dataset.

```python
from autoviz.AutoViz_Class import AutoViz_Class

AV = AutoViz_Class()

data = pd.read_csv("adult.csv")

AV.AutoViz(
    filename="adult.csv",
    sep=",",
    depVar="Income",
    dfte=data,
    chart_format="html"
)
```

---

## 📁 Project Structure

```text
EDA-Project/
│
├── adult.csv
├── EDA_Project_1.ipynb
└── README.md
```

---

## 📚 Key Concepts Covered

This project demonstrates practical understanding of:

* Data loading
* Data inspection
* Data selection
* Data filtering
* Aggregation
* GroupBy operations
* Descriptive statistics
* Missing-value handling
* Data cleaning
* Outlier detection
* IQR
* Z-score
* Winsorization
* Correlation analysis
* Data visualization
* Automated EDA

---

## 🚀 Conclusion

This project provides a practical introduction to **Exploratory Data Analysis using Python**.

Through this analysis, the Adult Income dataset was explored from multiple perspectives, including demographic characteristics, education, income, working hours, and other categorical and numerical attributes.

The project also demonstrates how data cleaning and visualization can be used together to identify patterns, relationships, inconsistencies, and potential outliers within a dataset.

---

## 👨‍💻 Author

**Nirup Koyilada**

B.Tech – Computer Science and Engineering
