# student-performance-analysis
Student Performance Analysis using Python, Pandas, and Matplotlib. Includes data cleaning, exploratory data analysis, correlation analysis, and visualizations of student academic performance.

#  Titanic Dataset Analysis
---

##  Objective
Analyze the Titanic dataset to discover survival patterns based on gender, passenger class, and age group using Python.

---

##  Dataset
- **Source:** [Kaggle – Titanic Dataset](https://www.kaggle.com/c/titanic)
- **Size:** 891 passengers × 15 columns
- **Key columns:** Survived, Pclass, Sex, Age, Fare, Embarked

---

##  Tools & Libraries
| Tool | Purpose |
|------|---------|
| Python | Programming language |
| Pandas | Data cleaning & analysis |
| Seaborn | Data visualization |
| Matplotlib | Data visualization |
| Google Colab | Development environment |

---

##  What I Did
1. Loaded and explored the Titanic dataset
2. Cleaned missing values:
   - `Age` → filled with median
   - `Embarked` → filled with mode
   - `Deck` → dropped (77% missing)
3. Analyzed survival patterns
4. Built visualizations

---

##  Questions Answered

### Q1: Who survived more — Males or Females?
| Gender | Survival Rate |
|--------|--------------|
| Female | 74%  |
| Male | 19%  |

>  Females were nearly 4x more likely to survive due to the "women first" evacuation rule.

### Q2: Did Passenger Class affect survival?
| Class | Survival Rate |
|-------|--------------|
| 1st Class | 63%  |
| 2nd Class | 47% |
| 3rd Class | 24%  |

>  1st class cabins were closer to the lifeboats on upper decks.

### Q3: What was the survival rate by age group?
| Age Group | Survival Rate |
|-----------|--------------|
| Children (0–12) | 58%  |
| Teens (13–18) | 43% |
| Young Adults (19–35) | 35% |
| Middle-Aged (36–60) | 40% |
| Seniors (61+) | 23%  |

>  Children were prioritized during evacuation.

---

##  Visualizations
- Bar chart – Survival rate by gender
- Bar chart – Survival rate by passenger class
- Histogram – Distribution of passenger ages

---

##  Conclusion
Three factors heavily influenced survival on the Titanic:
1. **Gender** – Females survived far more than males
2. **Class** – Wealthier passengers had better access to lifeboats
3. **Age** – Younger passengers, especially children, were prioritized

---

#  Titanic Dataset — Mini EDA

---

##  Objective
Perform a deeper Exploratory Data Analysis (EDA) on the Titanic dataset using
advanced data cleaning, feature engineering, and visualizations.

---

##  Dataset
- **Source:** [Kaggle – Titanic Dataset](https://www.kaggle.com/c/titanic)
- **Size:** 891 passengers × 15 columns

---

##  Tools & Libraries
| Tool | Purpose |
|------|---------|
| Python | Programming language |
| Pandas | Data cleaning & analysis |
| Seaborn | Data visualization |
| Matplotlib | Data visualization |
| Google Colab | Development environment |

---

##  What I Did
1. Loaded the Titanic dataset
2. Cleaned missing values:
   - `Age` → filled with mean
   - `Deck` → dropped (77% missing)
3. Engineered a new feature → `family_size = SibSp + Parch`
4. Analyzed 3 deeper questions
5. Built 3 professional visualizations

---

## Questions Answered

### Q1: Did Embarkation Port affect survival?
| Port | Survival Rate |
|------|--------------|
| Cherbourg (C) | 55%  |
| Queenstown (Q) | 39% |
| Southampton (S) | 34% |

>  Cherbourg had the most 1st class passengers — port didn't cause survival, wealth did!

### Q2: Did Family Size affect survival?
| Family Size | Survival Rate |
|-------------|--------------|
| 0 (alone) | 30% |
| 1 | 55% |
| 2 | 58% |
| 3 | 72% |
| 4 | 20% |
| 5+ | 14% |

>  Small families (1–3) helped each other. Solo travelers and large families struggled.

### Q3: Survival rate by Age Group?
| Age Group | Survival Rate |
|-----------|--------------|
| Child (0–12) | 58% |
| Teen (13–18) | 43% |
| Young Adult (19–30) | 33% |
| Adult (31–50) | 42% |
| Senior (51+) | 34% |

> Children were prioritized during evacuation.

---

## Visualizations
- Histogram – Age distribution with mean line
- Heatmap – Correlation between all variables
- Bar chart – Survival rate by family size

---

## Key Heatmap Findings
| Variables | Correlation | Meaning |
|-----------|------------|---------|
| pclass vs fare | -0.55 | Higher class = more expensive |
| survived vs pclass | -0.34 | Higher class number = lower survival |
| sibsp vs family_size | 0.89 | Strongly related (expected) |
| survived vs fare | 0.26 | Pricier ticket = slightly better survival |

---

## Conclusion
Three deeper factors influenced Titanic survival:
1. **Embarkation Port** – Driven by hidden wealth patterns behind each port
2. **Family Size** – Small families (size 3) had best survival (72%)
3. **Age Group** – Children were prioritized, seniors struggled most


# 📊 Titanic Mini Visualization Dashboard
### Data Science with Python Internship – Task 4

---

## 📌 Objective
Build a mini data visualization dashboard on the Titanic dataset
using 5 distinct chart types to communicate key insights visually.

---

## 📂 Dataset
- **Source:** [Kaggle – Titanic Dataset](https://www.kaggle.com/c/titanic)
- **Size:** 891 passengers × 15 columns

---

## 🛠️ Tools & Libraries
| Tool | Purpose |
|------|---------|
| Python | Programming language |
| Pandas | Data cleaning & feature engineering |
| Seaborn | Statistical visualizations |
| Matplotlib | Custom chart styling |
| Google Colab | Development environment |

---

## 🔍 What I Did
1. Cleaned missing values (Age → median, Embarked → mode, Deck → dropped)
2. Engineered 2 new features:
   - `family_size` = SibSp + Parch
   - `age_group` = Age bucketed into 5 categories
3. Built 5 distinct visualizations as a dashboard

---

## 📊 Dashboard Charts

| # | Chart Type | What it shows |
|---|-----------|---------------|
| 1 | Histogram | Age distribution with KDE curve |
| 2 | Bar Chart | Survival rate by class & gender combined |
| 3 | Boxplot | Fare distribution across passenger classes |
| 4 | Scatterplot | Age vs Fare colored by survival outcome |
| 5 | Heatmap | Correlations between all numeric variables |

---

## 💡 Key Insights

### 1. Age Distribution
- Most passengers were young adults (20–35)
- Right-skewed distribution — fewer older passengers

### 2. Survival by Class & Gender
- 1st class females: ~97% survival rate
- Gender was stronger predictor than class alone

### 3. Fare by Class (Boxplot)
- 1st class fares ranged wildly (£10–£170+)
- 3rd class fares were consistently low and clustered

### 4. Age vs Fare (Scatterplot)
- Higher fare passengers survived more (green dots at top)
- Age alone didn't predict survival — wealth did

### 5. Correlation Heatmap
| Variables | Correlation | Meaning |
|-----------|------------|---------|
| fare vs pclass | -0.55 | Higher class = more expensive |
| sibsp vs family_size | 0.89 | Built from same data |
| survived vs pclass | -0.34 | Lower class = lower survival |
| survived vs fare | +0.26 | Pricier ticket = better survival |

---

## 🏁 Conclusion
This dashboard reveals that survival on the Titanic was shaped by:
1. **Gender** — females survived far more across all classes
2. **Wealth** — higher fares and better class = better survival odds
3. **Age** — younger passengers had slight advantages
