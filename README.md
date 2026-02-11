# Streamlytics

# Netflix Content & Talent Analytics Platform

## 📌 Project Overview

This project provides a comprehensive analytical view of Netflix’s content library and talent performance. By leveraging structured metadata for titles and credits, the solution delivers actionable insights into content trends, audience preferences (IMDb vs. TMDB), and the impact of directors and cast members on show success.

The project was developed to move beyond raw data into a structured semantic model that supports data-driven decisions for content acquisition and production strategy.

## 📊 Business Objectives

* **Content Portfolio Analysis:** Identify trends across years, genres, and content types (Movies vs. TV Shows).
* **Ratings Evaluation:** Compare audience sentiment between IMDb and TMDB and identify top/low-performing content.
* **Talent Insights:** Analyze the association of specific directors and actors with highly-rated or popular titles.
* **Attribute Impact:** Evaluate how runtime, age certification, and season counts influence viewer ratings.

## 🗂️ Dataset Description

The analysis is based on two primary datasets:

1. **Titles Table:** Contains metadata for movies and shows (ID, title, release year, age certification, runtime, genres, production countries, IMDb/TMDB scores, and popularity).
2. **Credits Table:** Contains talent information linked to titles (Person ID, Name, Character, and Role—Director/Actor).

## 🛠️ Data Modeling & Transformation

To ensure analytical accuracy, the following transformations were performed in **Power Query**:

* **Genre Unpivoting:** Expanded nested genre lists into a normalized format to allow for accurate cross-filtering.
* **Data Cleaning:** Handled missing values in `age_certification` (labeled as "Unrated") and `imdb_id`.
* **Schema Architecture:** Implemented a **Star Schema** with the Titles table as a Dimension and the Credits table as a Fact/Detail table.

## 🚀 Key Features & KPIs

* **Executive Summary:** High-level view of total content, average ratings, and library growth over time.
* **Content Deep Dive:** Analysis of content count by type, genre, and year.
* **Ratings Analysis:** Scatter plot comparison of IMDb vs. TMDB scores and Top N content rankings.
* **Talent Leaderboard:** Top directors and actors ranked by average content rating and popularity.
* **Certification Distribution:** Breakdown of age ratings across the catalog to identify target demographics.

## 📈 Key Insights Derived

* **Genre Success:** Documentation, History, and War genres consistently achieve the highest average ratings.
* **Format Performance:** TV Shows generally command higher audience ratings compared to feature films.
* **Rating Platforms:** TMDB users tend to be more generous with scores, particularly for TV Shows and children's content, compared to IMDb users.
* **Talent Impact:** Specific directors (e.g., Martin Scorsese, Hayao Miyazaki) show a high correlation with top-tier IMDb scores in the Netflix library.

## 💻 How to Use

1. **Clone the Repository:** `git clone https://github.com/yourusername/netflix-analytics.git`
2. **Open the Report:** Launch the `Netflix_Dataset_Analysis.pbix` file using Power BI Desktop.
3. **Data Refresh:** The model is pre-configured to point to the provided CSV files. Update the data source paths in Power Query if you move the files.

## 📂 File Structure

* `Netflix_Dataset_Analysis.pbix`: The primary Power BI report file.
* `Netflix Data.xlsx - titles.csv`: Source data for content metadata.
* `Netflix Data.xlsx - credits.csv`: Source data for talent and cast.
* `BRD.docx`: The Business Requirement Document outlining project scope.

---

### 👨‍💻 Author

**Aniruddha Dutta** [[Aniruddha Dutta](https://www.linkedin.com/in/aniruddhadutta/)] 