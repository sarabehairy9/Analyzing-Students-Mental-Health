# Analyzing-Students-Mental-Health
Uncovering Mental Health Trends in International Students with PostgreSQL 📊✨
## table of content 
## Table of Contents  
- [Project Overview](#project-overview)  
- [Data Sources](#data-sources)  
- [Recommendations](#recommendations)  


### project overview 
##### This project explores the mental health impact on international students using PostgreSQL. Based on a 2018 study from a Japanese university, which found higher mental health risks among international students, we analyze student data to identify similar patterns. Key factors include social connectedness, acculturative stress, and the length of stay. Using SQL queries, we examine correlations to understand how studying abroad affects mental well-being.

### data sources
#### Analyzing international students' mental health using insights from students.csv

### tools 
- Excel -> data cleaning 
- ql-server -> data analysis

### data cleaning 
1. Load the Data
2. Handle Missing Values
### Exploring Mental Health Challenges
1. Do international students have a higher risk of mental health difficulties compared to local students?
2. Are students who report higher acculturative stress more likely to experience depression?
3. Do short-term exchange students face higher mental health challenges compared to long-term international students?

### data analysis 
```sql 
SELECT stay,
COUNT(*) AS count_int,
ROUND(AVG(todep), 2) AS average_phq,
ROUND(AVG(tosc), 2) AS average_scs,
ROUND(AVG(toas), 2) AS average_as 
FROM students
WHERE inter_dom = 'Inter'
GROUP BY stay
ORDER BY stay DESC;
```

### results
Trend in Mental Health Over Stay Duration
Higher PHQ (Patient Health Questionnaire) scores for short-term students indicate that they experience more depression, likely due to difficulties in adaptation, social isolation, and cultural stress.
lower PHQ (Patient Health Questionnaire) scores for long-term students suggest that extended stays help them adjust, build stronger support networks, and improve their mental well-being.

 ### recommendations 
 1. Support for Short-Term Students
 2. Encourage participation in student clubs
 3. support providing pre-arrival orientation programs and early intervention counseling to ease their transition.

### references
#### DataCamp. (n.d.). SQL for Data analysis . Retrieved from https://www.datacamp.com
#### PostgreSQL for Data Analysis



 





