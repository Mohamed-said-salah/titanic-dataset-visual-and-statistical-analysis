# 🛳️ Titanic Data Analysis — Exploratory Data Analysis (EDA) with Python & Seaborn

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1KWIiLfkRKNr6Psi1i0ArJszUQRkFwJlj?usp=sharing)

---

## 📘 Project Overview
This project performs a complete **Exploratory Data Analysis (EDA)** on the famous **Titanic dataset** using Python, Pandas, Seaborn, and Matplotlib — all inside **Google Colab**.

It explores how different passenger characteristics such as gender, class, age, and family size affected survival rates, and visualizes these patterns through professional-looking statistical plots.

---

## 🧩 Dataset

The dataset is loaded **directly from Seaborn** — no downloads or uploads required:

```python
import seaborn as sns
df = sns.load_dataset('titanic')
```

This dataset is a cleaned and well-structured version of the original Kaggle Titanic data, containing demographic and ticket information for 891 passengers aboard the Titanic.

### Key Columns

| Column | Description |
|:-------|:-------------|
| `survived` | Survival (0 = Died, 1 = Survived) |
| `pclass` | Passenger class (1 = Upper, 2 = Middle, 3 = Lower) |
| `sex` | Gender |
| `age` | Age in years |
| `sibsp` | Number of siblings/spouses aboard |
| `parch` | Number of parents/children aboard |
| `fare` | Ticket fare |
| `embarked` | Port of embarkation (C = Cherbourg, Q = Queenstown, S = Southampton) |
| `deck`, `class`, `who`, `adult_male`, etc. | Additional categorical features |

---

## 🧠 Project Objectives
- Explore dataset structure and handle missing values  
- Compute descriptive and grouped survival statistics  
- Visualize relationships between key passenger attributes  
- Draw meaningful insights and summarize findings  

---

## ⚙️ Technologies Used

| Library | Purpose |
|:---------|:---------|
| **Pandas** | Data manipulation & cleaning |
| **NumPy** | Numerical computation |
| **Seaborn** | Statistical visualization |
| **Matplotlib** | Custom plotting |
| **Google Colab** | Interactive notebook environment |

---

## 📊 Analysis & Visualizations

The notebook performs:

1. **Data Overview**
   - Dataset info, shape, missing values
   - Numerical and categorical summaries  

2. **Statistical Analysis**
   - Survival rate by gender, class, and age groups  

3. **Visual Exploration**
   - Survival counts  
   - Gender vs Survival  
   - Class vs Survival  
   - Age Distribution  
   - Age vs Fare Scatter  
   - Correlation Heatmap  
   - Deck and Embarkation patterns  

4. **Feature Relationships**
   - Gender × Class × Survival  
   - Family Size vs Survival  

Example visualization:

```python
sns.barplot(x='class', y='survived', hue='sex', data=df)
```

Result:

![Example Plot](https://seaborn.pydata.org/_images/seaborn-barplot-1.png)

---

## 📈 Main Insights

- 👩 **Females** had a survival rate around **74%**, much higher than males  
- 💼 **1st-class** passengers had the best odds of survival  
- 👶 **Children** under 12 had better chances than adults  
- 💰 **Fare** positively correlated with survival  
- 👨‍👩‍👧‍👦 **Small families** (≤ 4 members) survived more often  
- 🛏️ **Deck B & C** were among the safest  

---

## ▶️ How to Run

You can open and run the notebook directly in **Google Colab** — no setup required.

1. Go to [Google Colab](https://colab.research.google.com)
2. Click **File → Open Notebook → GitHub**
3. Paste this repository URL  
4. Click **Run All**

Or simply click the badge below 👇

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1KWIiLfkRKNr6Psi1i0ArJszUQRkFwJlj?usp=sharing)

---

## 💾 Output

At the end of the analysis, a cleaned dataset can be exported:

```python
df.to_csv('titanic_cleaned.csv', index=False)
```

---

## 📚 Future Enhancements

- Add **Machine Learning models** (e.g., Logistic Regression, Random Forest)  
- Implement **feature engineering** (titles, family groups, cabin letters)  
- Build an **interactive dashboard** with Streamlit or Plotly  

---

## 👨‍💻 Author

**Mohamed Saied**  
Senior Software Engineer (Mobile) @ RSI Tech  

📫 Connect on [LinkedIn](https://www.linkedin.com/in/geophmohamed) or view more projects on [GitHub](https://github.com/Mohamed-said-salah)
