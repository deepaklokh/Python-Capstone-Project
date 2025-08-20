<h1 align="center">
  💻  Python Fundamentals – Capstone Project  📊
</h1>

<p align="center">
  <b>A ten-task, end-to-end data-engineering workflow built with pandas & NumPy.</b><br>
  From raw CSVs → cleansing → transformation → aggregation → actionable output.
</p>

---

## 📑 Table of Contents
1.  Project Overview  
2.  Dataset Descriptions  
3.  Environment Setup  
4.  File Structure  
5.  Task Breakdown  
6.  Methodology & Implementation  
7.  Results & Deliverables  
8.  How to Run  
9.  Technologies Used  
10. Contributing  
11. License  
12. Author  
13. Screenshots  

---

## 1 Project Overview
> *“Data is the new oil — but only when it’s refined.”*  
> This capstone refines three raw datasets into business-ready insights.  
> You’ll see **ten incremental tasks** that illustrate core skills every data-analyst needs:  
> ingestion, cleaning, merging, conditional logic, aggregation, and filtered reporting.

---

## 2 Dataset Descriptions

| 📄 DataFrame | Columns (key) | Description |
|-------------|--------------|-------------|
| **Employee** | ID · Name · Gender · City · Age | Personal & location data |
| **Seniority** | ID · Designation Level (1–4) | Role hierarchy |
| **Project** | ID · Project · Project Cost · Status | Budget & completion status |

---

## 3 Environment Setup
Python ≥3.7 recommended
pip install pandas numpy notebook

text

---

## 4 File Structure
Python-Capstone-Project/
│
├─ Capstone_Project_Python.ipynb # notebook with all tasks
├─ data/
│ ├─ employee.csv
│ ├─ seniority.csv
│ ├─ project.csv
│ ├─ final_temp.csv
│ ├─ total_project_cost.csv
│ └─ final_dataframe.csv
└─ screenshots/
├─ task1.png
├─ task2.png
└─ … one per task

text

---

## 5 Task Breakdown
| # | Task | Key Action |
|---|------|------------|
| 1 | Create CSVs | Build & persist **Employee**, **Seniority**, **Project** tables |
| 2 | Impute Costs | Replace missing *Project Cost* with a running average |
| 3 | Split Names | Separate *First* / *Last* & drop the composite column |
| 4 | Merge | Combine all tables into **Final** |
| 5 | Bonus | +5 % cost for *Finished* projects |
| 6 | Demotion | ↓ designation for any *Failed* project; drop ineligible leads |
| 7 | Titles | Add “Mr.” / “Mrs.” prefix, remove *Gender* |
| 8 | Promotion | ↑ designation for age > 29 (min-clipped at 1) |
| 9 | Aggregation | Summarise total project cost per employee |
| 10 | City Filter | Display all rows where *City* contains “o” |

---

## 6 Methodology & Implementation
<details>
<summary>Click to expand</summary>

* **Data Ingestion** – `pd.read_csv()` / `to_csv()` ensure reproducibility.  
* **Imputation** – list conversion ➜ running-average loop ➜ overwrite `NaN`s.  
* **String Ops** – `str.split()`, `np.where()` for dynamic prefixes.  
* **Joins** – chained `merge()` on `ID`.  
* **Conditional Logic** – vectorised `np.where()` & boolean masks.  
* **Aggregation** – `groupby().sum()` for cost roll-ups.  
* **Validation** – `clip()` keeps designation between 1 and 4.  

</details>

---

## 7 Results & Deliverables

| 📁 File | Purpose |
|---------|---------|
| `employee.csv` | Cleaned employee data |
| `seniority.csv` | Original designation levels |
| `project.csv` | Imputed project table |
| `final_temp.csv` | Merged output (post-Task 8) |
| `total_project_cost.csv` | Per-employee cost summary |
| `final_dataframe.csv` | Filtered dataset for Task 10 |
| `Capstone_Project_Python.ipynb` | Executable notebook |

---

## 8 How to Run
1. **Clone** the repository.  
2. Ensure the *data* folder contains all CSVs.  
3. Launch Jupyter Notebook and open `Capstone_Project_Python.ipynb`.  
4. **Run all cells** (Tasks 1 → 10).  
5. Inspect the new / updated CSVs in *data/*.

---

## 9 Technologies Used
* 🐍 Python 3.x  
* 🐼 pandas  
* 📊 NumPy  
* 📓 Jupyter Notebook  

---

## 10 Contributing
Ideas & pull requests are welcome! Possible enhancements:
* Parameterise the bonus percentage.  
* Visualise cost distributions.  
* Convert the notebook into a CLI script.

---

## 11 License
**MIT** – free to use, modify, and distribute.

---

## 12 Author
**Deepak Lokhande** — Data-Analytics Enthusiast | Business Intelligence | Remote-Work Advocate  

---

## 13 Screenshots
*(Add one image per task in the `/screenshots` folder – each line below will render automatically.)*

![Task 1 – Create CSVs](screenshots/task1.png)  
![Task 2 – Impute Costs](screenshots/task2.png)  
![Task 3 – Split Names](screenshots/task3.png)  
![Task 4 – Merge DataFrames](screenshots/task4.png)  
![Task 5 – Add Bonus](screenshots/task5.png)  
![Task 6 – Demote / Prune](screenshots/task6.png)  
![Task 7 – Prefix Titles](screenshots/task7.png)  
![Task 8 – Promote Levels](screenshots/task8.png)  
![Task 9 – Total Cost Summary](screenshots/task9.png)  
![Task 10 – City Filter Output](screenshots/task10.png)
