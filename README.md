# 🛳 Titanic Dataset Analysis

This project performs exploratory data analysis (EDA) on the famous Titanic dataset using Python libraries such as Pandas, NumPy, Seaborn, and Matplotlib.
The goal is to understand survival patterns based on different features like class, gender, and age.
## 📂 Dataset

The dataset is downloaded from [Kaggle](https://www.kaggle.com/datasets/yasserh/titanic-dataset) using the `kagglehub` library and contains 891 rows with the following features:

- **PassengerId**: Unique ID for each passenger
- **Survived**: Survival status (0 = No, 1 = Yes)
- **Pclass**: Passenger class (1 = 1st, 2 = 2nd, 3 = 3rd)
- **Name, Sex, Age**: Personal information
- **SibSp, Parch**: Family aboard
- **Ticket, Fare**: Travel fare and ticket number
- **Cabin, Embarked**: Cabin and port of embarkation

---

## 🧼 Data Cleaning

- Missing **Age** values were filled with the **median**.
- **Cabin** values were transformed into a new column `deck` using the first letter (e.g., 'C85' → 'C'), and missing values filled as `'U'` (unknown).
- Two missing values in **Embarked** were filled with the mode.
- **Cabin** column was dropped after extracting `deck`.
- Categorical columns `Sex` and `Embarked` were mapped to numerical values.
- Dataset was confirmed to be free of **nulls** and **duplicates**.

---

## 📊 Exploratory Data Analysis

### 🔢 Summary Statistics

- Total passengers: **891**
- Survival rate: **38.4%**
- Median age: **28**
- Max fare: **512**

### 📈 Visual Insights

#### 🔹 Survival Distribution
- **342 passengers survived**, while **549 did not**.
- The **survival rate is lower** than the non-survival rate.

#### 🔹 Survival by Class
- Most survivors were from **Class 1**, followed by **Class 3** and **Class 2**.
- Among non-survivors, **Class 3** had the highest count, then **Class 2**, then **Class 1**.

#### 🔹 Survival by Gender
- **~250 females survived**, while fewer than **100 did not**.
- Among males, **over 400 did not survive**, while between **100 and 140 survived**.

#### 🔹 Outliers
- The **Fare** feature contains several outliers, as seen in the boxplot.
- **Age** shows a more normal distribution with a few extreme values.
