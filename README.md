# 📊 Practical 4 — Understanding Data with Graphs

> Exploring the TeachingRatings dataset through statistical analysis and data visualization using Python.

---

## 🎯 Objective

To understand and analyze data using graphs and statistical techniques
by exploring relationships between instructor age, teaching evaluations,
course division, gender, and tenure status.

---

## 📚 Practical Overview

This practical uses the **AER TeachingRatings dataset** to perform
statistical analysis and create meaningful visualizations.

The analysis focuses on:

- Duplicate cases and unique instructors
- Age analysis
- Course division and teaching evaluations
- Relationship between age and teaching evaluation
- Gender-differentiated analysis
- Gender and tenure analysis
- Data visualization

---

## 📊 Dataset

The practical uses the **AER TeachingRatings dataset**.

The dataset contains:

- **463 evaluated course observations**
- **94 unique professors**

Because professors may teach multiple courses, the same instructor
can appear in multiple rows of the dataset.

---

## 🔍 Analysis Performed

### 1. Duplicate Cases and Age Analysis

Since an instructor may teach multiple courses, calculating statistics
directly from course-level observations can give greater weight to
professors who teach more courses.

The dataset is therefore deduplicated using the instructor identifier
`prof`, resulting in **94 unique instructors**.

| Data Group | Observations | Mean Age | Std. Deviation |
|---|---:|---:|---:|
| All Observations | 463 | 48.3650 | 9.8027 |
| Unique Instructors | 94 | 47.5532 | 10.2565 |

The average age is slightly higher when calculated across all course
observations than across unique instructors.

---

### 2. Course Division and Teaching Evaluation

Teaching evaluations are compared between lower-division and
upper-division courses.

| Division | Average Evaluation Score |
|---|---:|
| Lower | 4.09 |
| Upper | 3.95 |

Lower-division courses have a slightly higher average teaching
evaluation score than upper-division courses.

---

### 3. Relationship Between Age and Teaching Evaluation

A **scatter plot with an Ordinary Least Squares (OLS) trendline** is
used to examine the relationship between instructor age and teaching
evaluation.

The visualization shows a wide distribution of evaluation scores
across different age groups.

The fitted regression line has a modest negative slope, indicating that
older professors receive slightly lower average evaluation scores in
this dataset.

---

### 4. Gender-Differentiated Analysis

The relationship between instructor age and teaching evaluation is
examined separately for male and female instructors.

The visualization helps compare:

- Evaluation score distributions
- Age patterns
- Gender differences

Both male and female instructors show a wide distribution of evaluation
scores across the age spectrum.

The analysis indicates that male instructors are more heavily represented
in the higher evaluation range above 4.5 across multiple age groups.

---

### 5. Gender and Tenure Analysis

Gender and tenure status are incorporated into a combined scatter plot.

The visualization uses:

- **Gender** to differentiate instructor groups
- **Marker shape** to represent tenure status

The analysis shows that:

- Non-tenured faculty tend to cluster in younger age categories.
- Tenured faculty extend into higher age categories.
- Female non-tenured professors show varied evaluation ratings.
- Male tenured faculty account for many of the high-evaluation points
  among instructors aged 50+.

---

## 📈 Visualizations

The practical includes several data visualizations:

### Course Division vs Teaching Evaluation

A bar chart compares average teaching evaluation scores for lower and
upper course divisions.

### Age vs Teaching Evaluation

A scatter plot with an OLS trendline illustrates the relationship between
instructor age and teaching evaluation.

### Age, Evaluation and Gender

A gender-differentiated scatter plot compares evaluation patterns
across instructor ages.

### Age, Evaluation, Gender and Tenure

A combined visualization examines the interaction between:

- Age
- Teaching evaluation
- Gender
- Tenure status

---

## 🛠️ Technologies Used

| Technology | Purpose |
|---|---|
| Python | Programming language |
| Pandas | Data manipulation and analysis |
| NumPy | Numerical computing |
| Matplotlib | Data visualization |
| Seaborn | Statistical visualization |
| Jupyter Notebook | Development environment |

---

## 📌 Key Concepts

### Deduplication

Removing repeated instructor records when professor-level analysis is
required.

### Group-wise Analysis

Comparing statistics across categories such as gender, tenure, or
course division.

### Scatter Plot

Used to visualize the relationship between two numerical variables.

### OLS Trendline

A fitted regression line used to identify the general linear direction
of a relationship.

### Bar Chart

Used to compare numerical values across categorical groups.

---

## 💻 Implementation

### Import Libraries

```python
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
