# Investigating Netflix Movies

## 📊 Project Overview

Data analysis project investigating trends in Netflix movie durations and content patterns using Python. This exploratory analysis examines whether movies are getting shorter over time and explores various content characteristics.

## 🎯 Research Questions

1. Are Netflix movies getting shorter over the years?
2. How does movie duration vary by genre?
3. What are the content trends on Netflix?
4. Are there patterns in release dates and content types?

## 🛠️ Tools & Technologies

- **Python:** Core programming language
- **pandas:** Data manipulation and analysis
- **matplotlib:** Data visualization
- **seaborn:** Statistical visualization
- **NumPy:** Numerical computations
- **Jupyter Notebook:** Interactive analysis environment

## 📁 Dataset

**Source:** Netflix Movies Dataset

**Features:**
- Movie titles
- Release year
- Duration (minutes)
- Genre categories
- Director and cast information
- Country of production
- Date added to Netflix

## 🔍 Analysis Workflow

### 1. Data Loading & Inspection
```python
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns

# Load and explore data
df = pd.read_csv('netflix_data.csv')
df.info()
df.describe()
```

### 2. Data Cleaning
- Handling missing values
- Data type conversions
- Filtering relevant movie records
- Creating derived features

### 3. Exploratory Data Analysis
- Duration trend analysis over years
- Genre-based comparisons
- Statistical distributions
- Correlation analysis

### 4. Visualization
- Time series plots
- Distribution histograms
- Box plots by genre
- Scatter plots for relationships

## 📈 Key Findings

1. **Duration Trends:**
   - Average movie duration shows slight decline over time
   - Variation increases in recent years (more short and long films)

2. **Genre Patterns:**
   - Action movies tend to be longer (avg. 110 min)
   - Comedies and documentaries are typically shorter (avg. 90 min)
   - Genre diversity has increased

3. **Content Growth:**
   - Exponential growth in content additions post-2015
   - Shift towards more international content

4. **Release Patterns:**
   - Most content added in Q4 (October-December)
   - Strong representation of recent productions (2015+)

## 💻 Code Highlights

### Statistical Analysis
```python
# Analyze duration trends
yearly_avg = df.groupby('release_year')['duration'].mean()
genre_duration = df.groupby('genre')['duration'].describe()
```

### Visualization
```python
# Create trend visualization
plt.figure(figsize=(12, 6))
plt.scatter(df['release_year'], df['duration'], alpha=0.5)
plt.xlabel('Release Year')
plt.ylabel('Duration (minutes)')
plt.title('Netflix Movie Duration Trends')
```

## 🎓 Skills Demonstrated

- **Data Wrangling:** Cleaning and preparing real-world data
- **Statistical Analysis:** Hypothesis testing and trend identification
- **Python Programming:** pandas, matplotlib, seaborn
- **Data Visualization:** Creating insightful charts
- **Critical Thinking:** Drawing conclusions from data

## 📊 Visualizations Created

1. **Scatter Plot:** Duration vs. Release Year
2. **Box Plot:** Duration by Genre
3. **Histogram:** Distribution of Movie Durations
4. **Line Chart:** Average Duration Trend Over Time
5. **Bar Chart:** Content Count by Genre

## 💡 Insights & Recommendations

### For Content Creators:
- Consider genre-appropriate durations
- Balance portfolio with various lengths

### For Netflix:
- Diverse duration strategy appeals to different audiences
- Short-form content gaining popularity

### For Viewers:
- Wide variety of content lengths available
- Genre can be indicator of expected duration

## 📚 Learning Outcomes

This project demonstrates:
- End-to-end data analysis workflow
- Python data science libraries proficiency
- Statistical thinking and hypothesis testing
- Data storytelling through visualization
- Documenting analysis for reproducibility

## 🔄 Future Enhancements

- Incorporate user ratings analysis
- Compare Netflix vs. other platforms
- Predictive modeling for content success
- Sentiment analysis of descriptions
- Network analysis of directors/actors

---

*This project showcases fundamental data analysis skills using Python and demonstrates the ability to extract meaningful insights from real-world datasets.*
