# 🎬 Netflix Power BI Dashboard  

## 📊 Project Overview  
This project presents an **interactive Power BI dashboard** built to analyze Netflix’s vast content library.  
It visualizes insights on **Movies and TV Shows** across countries, release years, ratings, and directors — helping understand Netflix’s global content strategy and growth patterns.  

---

## 🎯 Objectives  
- Analyze the **total number of Movies and TV Shows** on Netflix.  
- Explore **content release trends** over time.  
- Identify **leading countries** in content production.  
- Examine **content ratings and genres** distribution.  
- Enable **interactive filtering** by Show Type, Release Year, and Country.  

---

## 🧩 Dashboard Features  

| 🔍 Visual | 🧠 Description |
|------------|----------------|
| **Cards** | Show key metrics – Total Movies, Total TV Shows, and Overall Shows. |
| **Donut Chart (Type)** | Visualize the proportion of Movies vs TV Shows. |
| **Line Chart (Release Year)** | Observe content production trends over decades. |
| **Donut Chart (Directors)** | Display total number of directors involved. |
| **Map (Country)** | View geographical distribution of Netflix content. |
| **Bar Chart (Rating)** | Analyze the spread of shows by maturity rating. |

---

## 📈 Key Insights  
- 📺 **Total Content:** 8,807 titles  
- 🎞️ **Movies:** 6,131 (≈70%)  
- 📡 **TV Shows:** 2,676 (≈30%)  
- 🎬 **Total Directors:** 4,527  
- 🚀 Netflix’s content production **skyrocketed post-2015**, reflecting global expansion.  
- 🔞 **TV-MA** and **TV-14** dominate, showing focus on mature audiences.  
- 🌍 **USA, India, and UK** lead in total content creation.  

---

## ⚙️ Tools & Technologies  
- **Power BI Desktop** – Dashboard creation and visualization  
- **Power Query Editor** – Data cleaning and transformation  
- **DAX (Data Analysis Expressions)** – Custom measures and KPIs  
- **Excel / CSV Dataset** – Source data for analysis  

---

## 🧾 Dataset Description  
| Column | Description |
|---------|--------------|
| `show_id` | Unique ID of the show |
| `type` | Movie / TV Show |
| `title` | Name of the content |
| `director` | Director name |
| `country` | Country of origin |
| `date_added` | Date added to Netflix |
| `release_year` | Year of release |
| `rating` | Audience rating (e.g., TV-MA, PG-13) |
| `duration` | Length (minutes / seasons) |
| `listed_in` | Genre / category |
| `description` | Short summary of the content |

---

## 🧮 DAX Measures Used  

```DAX
Total Movies = CALCULATE(COUNTROWS(Netflix), Netflix[type] = "Movie")
Total TV Shows = CALCULATE(COUNTROWS(Netflix), Netflix[type] = "TV Show")
Total Shows = COUNTROWS(Netflix)
Total Directors = DISTINCTCOUNT(Netflix[director])
