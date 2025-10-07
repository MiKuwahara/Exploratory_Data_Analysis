# 📊 Exploratory Data Analysis (EDA) Lab

This project explores key techniques in **Exploratory Data Analysis (EDA)** using Python.  
It builds on a cleaned dataset to investigate data distribution, outliers, and correlations between features.



## 🚀 Overview
The goal is to understand the dataset’s structure and relationships before modeling.  
You’ll explore distributions, detect and remove outliers, and compute feature correlations.



## 🧠 Tools & Skills
- Python  
- Pandas, NumPy, Matplotlib, Seaborn  
- Outlier detection (IQR)  
- Data visualization  
- Correlation analysis  



## 🗂️ Dataset
Developer survey data containing salary (`ConvertedComp`), age, work hours, and gender.  
📁 Source:  
`https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/IBM-DA0321EN-SkillsNetwork/LargeData/m2_survey_data.csv`


## 🔍 Key Analysis Steps

### 1. Distribution Analysis
- Visualized salary distribution using histograms and kernel density plots.  
- The median salary is **$57,745** for all responders, while the median salary for **women responders is $57,708**, indicating a nearly identical median pay level across genders.
- The salary distribution is **highly right-skewed**, meaning the majority of respondents earn on the lower end, with a few individuals earning extremely high salaries.
- **Outliers** (1M-2M+ salaries) significantly stretch the scale, making it difficult to see details in the lower range.
- The **KDE curve** shows a sharp peak near the lower salary range, confirming that most respondents fall in that region.
- Due to this skew, the **mean salary is likely higher than the median**, suggesting that the data is influenced by a small number of very high earners.

### 2. Outlier Detection & Removal
- Calculated the **Interquartile Rnage (IQR)** to identify extreme salary values beyond the upper and lower bounds.
- Found **879 outliers**, mainly representing individuals with **exceptionally high salaries (above $250,00)**.
- These outliers caused the distribution to be highly right-skewed, distorting measures such as the mean and making it harder to interpret the overall salary pattern.
- After removing outliers, the **median salary decreased** from **$57,745 to $52,704**, indicating that the original median was slightly inflated by high-income earners.
- The **cleaned dataset** provides a more accurate picture of the **typical salary range** for most respondents and allows for more reliable comparisons and statistical analysis in subsequent steps. 

### 3. Correlation Analysis
- **Weak positive correlation** between **Age** and **ConvertedComp (Salary)** *(r = 0.105)*, suggesting that older respondents tend to earn slightly higher salaries, though the relationship is not strong.  
- **Negative correlation** between **CodeRevHrs** (hours spent on code review) and **Age**, indicating that younger developers spend more time on code reviews compared to older peers.  
- Most correlations among other numeric variables were **weak or near zero**, implying limited linear relationships between demographic factors and salary-related variables.  
- These findings highlight that while **age has a mild influence on salary**, other factors beyond age likely play a larger role in determining compensation.

  



## 📓 Notebook
📘 [View the EDA Notebook](./ExploratoryDataAnalysis.ipynb)



## 📚 What I Learned
- Identify and visualize data distributions  
- Detect and handle outliers  
- Interpret correlation matrices  
- Summarize and communicate insights effectively  

