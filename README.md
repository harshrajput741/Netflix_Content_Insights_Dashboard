🎬 Netflix Dashboard Project – What to Include
✅ 1. Project Overview

Project Title:
Netflix Content Insights Dashboard

Objective:
To analyze Netflix’s movies and TV shows dataset and extract meaningful insights about content distribution, ratings, genres, and trends using interactive visualizations.

🛠️ 2. Tools & Technologies Used
🔹 Primary Tools
Category	Tools
Data Visualization	Power BI
Data Transformation	Power Query
Data Modeling	DAX (Data Analysis Expressions)
Data Source	CSV (Netflix Dataset from Kaggle)
🔹 Optional/Supporting Tools
Category	Tools
Data Cleaning	Python (Pandas) (optional)
Version Control	Git & GitHub
Documentation	Microsoft Word / Notion / README
Design	PowerPoint / Figma (for layout planning)
🧠 3. Languages Used
Language	Purpose
DAX	Creating measures and calculated columns
M Language	Data transformation in Power Query
SQL (Optional)	Data extraction if using a database
Python (Optional)	Advanced data cleaning and EDA
📊 4. Data Preparation (ETL Process)
🔹 Extract
Imported the Netflix dataset from a CSV file.
🔹 Transform
Cleaned missing values.
Removed duplicates.
Standardized column names.
Split multi-value columns like genres and production_countries into rows.
Converted data types (e.g., runtime to numeric).
Created a new column Content Category (Adult, Teen, Kids).
🔹 Load
Loaded the transformed data into Power BI for analysis.
📐 5. Data Modeling
Built relationships between tables (if applicable).
Created calculated columns and measures using DAX.
Optimized the data model for performance.
🔹 Example DAX Measures
Total Titles = COUNT('Netflix'[title])

Avg IMDB Score = AVERAGE('Netflix'[imdb_score])

Avg TMDB Score = AVERAGE('Netflix'[tmdb_score])

Total Votes = SUM('Netflix'[imdb_votes])

Total Countries = DISTINCTCOUNT('Netflix'[production_countries])
🔹 Content Category Column
Content Category =
SWITCH(
    TRUE(),
    'Netflix'[age_certification] IN {"TV-MA", "R"}, "Adult",
    'Netflix'[age_certification] IN {"TV-14", "PG-13"}, "Teen",
    'Netflix'[age_certification] IN {"PG", "TV-Y7", "TV-Y", "G"}, "Kids",
    "Unknown"
)
📊 6. KPIs Created
KPI	Description
Total Titles	Total number of movies and TV shows
Average IMDb Score	Overall content quality
Average TMDB Score	Additional rating comparison
Total IMDb Votes	Popularity indicator
Average Runtime	Average duration of content
Total Countries	Geographic diversity
📈 7. Visualizations Included
Visualization	Purpose
KPI Cards	Display key metrics
Line Chart	Content growth over the years
Bar Chart	Movies vs TV Shows
Bar Chart	Top Genres
Bar Chart	Top Production Countries
Histogram	IMDb Score distribution
Scatter Plot	Runtime vs IMDb Score
Bar/Pie Chart	Age Certification distribution
Table	Top 10 highest-rated titles
Slicers	Interactive filtering (Type, Genre, Year)
