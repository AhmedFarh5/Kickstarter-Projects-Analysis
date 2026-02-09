#  Kickstarter Projects Analysis — Power BI

##  Data Source

Dataset obtained from Kaggle:
[https://www.kaggle.com/kemical/kickstarter-projects](https://www.kaggle.com/kemical/kickstarter-projects)

* Two CSV files used:

  * 2016 Projects
  * 2018 Projects

---

## 🔄 Data Transformation (Power Query — M Language)

The following preparation steps were performed:

* Created a **Custom Column** containing the source file name
  (e.g., `2016`, `ks-projects-201612`)
* Appended (Union) the two datasets into one combined table
* Renamed the final table to a clear name (e.g., `ALLdata`)
* Removed/hidden intermediate tables from the model view

---

##  Data Modeling

* Created a hierarchy:

  * Main Category
  * Category
  * Project Name
    Named **Project Hierarchy**
* Organized and renamed tables in the model
* Built the following measures:

DAX
Number of Projects = COUNT(KSProjects[Project Name])
Number of Backers = SUM(KSProjects[Backers])
Total Pledged = SUM(KSProjects[Pledged])
Total Goal = SUM(KSProjects[Goal])


---

##  Visualizations

Using the measures above:

### KPI Cards

* Number of Projects
* Number of Backers
* Total Pledged
* Total Goal

### Charts

* Number of Projects by State
* Number of Projects by Project Hierarchy (Drill Down)
* Number of Projects by Launch Date
* Total Pledged by Currency or Country

---

##  Design Considerations

* Meaningful chart titles
* Clean layout
* Consistent color palette
* Clear storytelling through visuals

---

##  Objective

Practice data preparation, modeling, and visualization in Power BI while exploring crowdfunding trends across Kickstarter projects.

---

## 👤 Author

Ahmed Mohamed
Data Science Student — Helwan University
