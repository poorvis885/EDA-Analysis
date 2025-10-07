# 🚢 Titanic Survival Analysis & Exploratory Data Analysis (EDA)

## 📌 Project Overview
This project explores the famous **Titanic Dataset** to analyze survival trends based on different factors such as gender, passenger class, and age.  
Using **Pandas, Seaborn, Matplotlib, and hypothesis testing**, we uncover key insights into what influenced survival rates.

---

## 📊 Key Features
- ✅ **Data Cleaning:** Handling missing values & dropping irrelevant columns.  
- ✅ **Survival Analysis:** Investigating survival trends based on gender, class, and age.  
- ✅ **Visualizations:** Stunning plots to reveal insights.  
- ✅ **Hypothesis Testing:** Statistical validation using **Chi-Square & T-tests**.  

---

## 📂 Dataset Source
The dataset contains information on Titanic passengers with the following key columns:  

- `Survived` → 0 = No, 1 = Yes  
- `Pclass` → Ticket class (1st, 2nd, 3rd)  
- `Sex` → Male / Female  
- `Age` → Passenger's age  
- `Fare` → Price paid for the ticket  
- `Embarked` → Port of embarkation (C, Q, S)  

---

## 📦 Installation & Usage

1️⃣ Clone the repository  
```bash
git clone https://github.com/your-username/titanic-eda.git
cd titanic-eda


2️⃣ Install dependencies
```bash
pip install pandas numpy matplotlib seaborn scipy


3️⃣ Run the script
```bash
python titanic_eda.py
📈 Exploratory Data Analysis (EDA)
🔹 Survival Rate by Gender

Insight: Women had a much higher survival rate than men.
sns.barplot(x='Sex', y='Survived', data=df, palette='pastel')

🔹 Survival Rate by Class

Insight: 1st class passengers had a higher survival rate.
sns.barplot(x='Pclass', y='Survived', data=df, palette='pastel')

🔹 Age Distribution (Survivors vs Non-Survivors)

Insight: Young children had higher survival rates.
sns.histplot(df[df['Survived'] == 1]['Age'], bins=30, color='green', kde=True)
sns.histplot(df[df['Survived'] == 0]['Age'], bins=30, color='red', kde=True)
```bash

🧪 Hypothesis Testing
📌 1. Chi-Square Test (Gender & Survival)

Question: Does gender affect survival?
Result: Yes, gender played a significant role.
chi2, p, _, _ = chi2_contingency(pd.crosstab(df['Sex'], df['Survived']))
if p < 0.05:
    print("Gender and survival rate are statistically dependent.")

📌 2. T-Test (Age & Survival)

Question: Did age affect survival?
Result: No strong evidence that age played a major role.
t_stat, p_value = ttest_ind(df[df['Survived'] == 1]['Age'],
                            df[df['Survived'] == 0]['Age'])

📌 Conclusion

✅ Women and children had a higher survival rate.

✅ 1st class passengers had better chances of survival.

✅ Age was not a significant factor in survival.
🤝 Contributing

Feel free to fork this repository and submit pull requests! 🚀

💡 Want to contribute? Star ⭐ the repo, raise issues, and improve it!
🔗 Connect with Me

👩‍💻 LinkedIn – Poorvi Shrivastava
