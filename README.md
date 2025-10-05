📊 Netflix Power BI Analysis Dashboard
📁 Project Overview

This Power BI dashboard provides a comprehensive analysis of Netflix’s content library, focusing on Movies and TV Shows across different countries, release years, and ratings. The visualization helps uncover insights into Netflix’s content distribution, production trends, and audience targeting over time.

🎯 Objectives

Analyze the total number of Movies and TV Shows available on Netflix.

Visualize content growth trends based on release years.

Identify top contributing countries to Netflix’s content library.

Examine distribution of shows by type, rating, and directors.

Provide interactive filtering for Show Type, Release Year, and Country.

📈 Key Insights

Total Shows: 8,807

Movies: 6,131 (≈70%)

TV Shows: 2,676 (≈30%)

Total Directors: 4,527

Peak content release occurred after 2015, highlighting Netflix’s massive production expansion.

TV-MA and TV-14 ratings dominate, showing Netflix’s focus on mature audiences.

The USA, India, and UK lead in content production.

🧩 Dashboard Features
Visual	Description
Card Visuals	Display total counts of Movies, TV Shows, and overall content.
Pie Chart – Total Shows by Type	Compares Movies vs TV Shows percentage.
Line Chart – Total Shows by Release Year	Shows Netflix content growth trend over time.
Pie Chart – Total Directors	Represents director contributions across content types.
Map – Total Shows by Country	Highlights geographical distribution of Netflix content.
Bar Chart – Total Shows by Rating	Displays the distribution of content by maturity rating.
⚙️ Tools and Technologies

Power BI Desktop – Data visualization and dashboard creation

Excel / CSV dataset – Netflix dataset (contains ~8.8K rows, 12+ columns)

DAX (Data Analysis Expressions) – Used for measures and KPIs

Data Cleaning & Transformation – Power Query Editor

📂 Dataset Description

The dataset includes the following key columns:

show_id – Unique ID of the show

type – Movie / TV Show

title – Name of the content

director – Director of the show

country – Country of origin

date_added – Date content was added to Netflix

release_year – Original release year

rating – Audience rating (e.g., TV-MA, PG-13)

duration – Duration in minutes or seasons

listed_in – Genre/category

description – Short content summary

🧮 DAX Measures Used
Total Movies = CALCULATE(COUNTROWS(Netflix), Netflix[type] = "Movie")
Total TV Shows = CALCULATE(COUNTROWS(Netflix), Netflix[type] = "TV Show")
Total Shows = COUNTROWS(Netflix)
Total Directors = DISTINCTCOUNT(Netflix[director])

🧠 Insights & Business Impact

The rapid growth in content post-2015 indicates Netflix’s global expansion strategy.

Dominance of mature content (TV-MA) suggests a focus on adult audiences.

Regional analysis helps identify emerging content-producing markets.

The dashboard can guide content acquisition and localization strategies.
