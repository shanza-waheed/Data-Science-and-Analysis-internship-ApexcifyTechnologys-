# 📊 Student Performance Analysis  

This project was completed as part of my **Data Analysis Internship at Apexcify Technologies**.  
The goal of this project is to analyze student performance across multiple subjects, calculate their average scores, and identify the top-performing student using Python and Pandas.  

---

## 📌 Project Overview  
The dataset contains the scores of students in three subjects: **Math, English, and Science**.  
By applying data analysis techniques, we calculated each student’s average and highlighted the top scorer.  

---

## 📂 Dataset  
The dataset used is `students.csv` with the following columns:  
- **Name** – Student's name  
- **Math** – Marks in Mathematics  
- **English** – Marks in English  
- **Science** – Marks in Science  

Example Data:  

| Name  | Math | English | Science |
|-------|------|---------|---------|
| Ayan  | 80   | 75      | 90      |
| Sara  | 92   | 88      | 95      |
| Bilal | 76   | 69      | 72      |
| Mehak | 88   | 80      | 94      |
| Zara  | 95   | 85      | 91      |

---

## 🎯 Objectives  
- Load and explore the dataset  
- Compute the average marks for each student  
- Identify the highest-scoring student  
- Display results in a clean tabular format  

---

## 🛠️ Tools & Libraries  
- **Python**  
- **Pandas**  

---

## 🔎 Implementation  

### Step 2: Calculate Average Marks for Each Student  
```python
import pandas as pd

# Load dataset
df = pd.read_csv("students.csv")

# Calculate average marks across Math, English, and Science
df["Average"] = df[["Math", "English", "Science"]].mean(axis=1)

print("Student Data with Averages:")
print(df)
```
### Step 3: Identify the Highest Average Scorer  
```python
# Find the student with the highest average
highest_avg_student = df.loc[df["Average"].idxmax()]

print("\nTop Performing Student:")
print(highest_avg_student)
```
### Step 4: Display Results  
```python
print("Final DataFrame with Averages:")
print(df)

print("\nHighest Scoring Student Details:")
print(highest_avg_student)
```
## 📊 Results  
- Average marks successfully calculated for each student  
- Highest-performing student identified  

### Student Data with Averages  
```python
print(df)
```
## 🏆 Top Student Result  

After calculating the averages, the highest-performing student was identified as:  

##Top Student:
| Name  | Math | English | Science | Average |
|-------|------|---------|---------|---------|
| Sara  | 92   | 88      | 95      | 91      |
