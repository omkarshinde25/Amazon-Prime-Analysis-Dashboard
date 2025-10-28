# Amazon Prime Video Data Analysis Dashboard

## Project Overview
This project, titled Amazon Prime Video Data Analysis Dashboard, presents an end-to-end data analysis and visualization solution built using Microsoft Power BI. The objective of this project is to analyze Amazon Prime Video’s content catalog, explore its global distribution, and understand patterns across genres, release years, countries, and content types (Movies and TV Shows).

By leveraging Power Query for data cleaning and transformation, along with DAX (Data Analysis Expressions) for calculations, this project demonstrates how raw data can be converted into meaningful business insights. The final interactive dashboard provides a clear, data-driven picture of Amazon Prime Video’s content diversity, growth trends, and strategic content distribution over time.

---
## Dashboard -<br>

<img src="https://github.com/omkarshinde25/Amazon-Prime-Analysis-Dashboard/blob/main/Dashboard%20PNG/Amazon%20Prime%20Analysis.png" width="800"> <br>

---

1. Amazon Prime Video hosts a total of 9,655 titles across movies and TV shows.
2. Movies form 81% of the catalog, while TV shows contribute 19%.
3. The United States, India, and the United Kingdom produce the highest volume of content.
4. Drama, Comedy, and Documentary are the most common genres on the platform.
5. A major increase in content was observed between 2010 and 2020.
6. Ratings 13+ and TV-MA appear most frequently across all titles.
7. The average movie duration lies between 90 and 120 minutes.
8. Prime Video content covers over 80 countries globally.
9. Many older titles were added to the platform in recent years, showing active licensing growth.
10. The dashboard highlights Amazon Prime Video’s strong global presence and diverse content strategy.

---

## Step 1: Dataset Overview
The dataset was obtained from Kaggle’s Amazon Prime Titles Dataset and contains information on movies and TV shows available on Amazon Prime Video.

- Show ID
- Type (Movie / TV Show)
- Title
- Director
- Cast
- Country
- Date Added
- Release Year
- Rating
- Duration
- Genre (Listed In)
- Description

**Total Records:** 9,655  
**File Type:** CSV / Excel  
**Source:** Kaggle Public Dataset

---

## Step 2: Data Cleaning and Transformation (ETL)
Performed using Power Query Editor in Power BI.

### Key Transformations:
- Removed 82 duplicate and blank records.
- Filled missing values with “Not Available.”
- Standardized columns and data types.
- Extracted year from “Date Added.”
- Split genres for better filtering.
- Trimmed spaces and removed special characters.
- Corrected release year and rating inconsistencies.

---

## Step 3: Data Modeling and DAX Calculations
Relationships were created, and DAX measures were implemented for KPIs.

### Example DAX Measures:
```
Total Titles = COUNT(amazon_prime_titles[show_id])
Total Movies = CALCULATE(COUNT(amazon_prime_titles[show_id]), amazon_prime_titles[type] = "Movie")
Total TV Shows = CALCULATE(COUNT(amazon_prime_titles[show_id]), amazon_prime_titles[type] = "TV Show")
Distinct Ratings = DISTINCTCOUNT(amazon_prime_titles[rating])
Distinct Genres = DISTINCTCOUNT(amazon_prime_titles[listed_in])
Earliest Year = MIN(amazon_prime_titles[release_year])
Latest Year = MAX(amazon_prime_titles[release_year])
```

---

## Step 4: Dashboard Design and Development
- Clean UI using modern Power BI visuals.
- Blue-black-gray theme.
- Interactive slicers for Type, Country, Rating, and Year.
- KPI cards for quick insights.

---

## Step 5: Visualizations Created
- **Pie Chart:** Movies vs. TV Shows.  
- **Bar Chart:** Content by Country.  
- **Line Chart:** Year-wise growth trend.  
- **Donut Chart:** Genre distribution.  
- **Map Chart:** Global content coverage.  
- **KPI Cards:** Total Titles, Ratings, Genres.

---

## Step 6: Insights and Findings
- Amazon Prime Video hosts 9,655 titles (81% Movies, 19% TV Shows).
- Top producing countries: USA, India, UK.
- Popular genres: Drama, Comedy, Documentary.
- Peak release years: 2010–2020.
- Common ratings: 13+, TV-MA.
- Global coverage with strong presence in North America and Asia.

---

## Step 7: Tools and Technologies Used
- Power BI  
- Power Query Editor  
- DAX  
- Excel  
- Kaggle Dataset

---

## Step 8: Project Outcome
The dashboard delivers a comprehensive overview of Amazon Prime’s content ecosystem. It highlights how data storytelling and DAX modeling bring strategic insights to life.

---

## Step 9: How to Use
1. Download the dataset from Kaggle.  
2. Open “Amazon Prime Analysis.pbix” in Power BI.  
3. Connect the dataset.  
4. Explore using filters and slicers.  

---

## Step 10: Key Learning and Skills Demonstrated
- Data Cleaning and ETL  
- Advanced DAX  
- Interactive Power BI Dashboards  
- Data Modeling  
- Visualization and Storytelling  

---

## Conclusion
This project demonstrates the complete process of transforming raw data into actionable insights using Microsoft Power BI. It reflects analytical thinking, data visualization expertise, and a passion for data-driven decision-making.

