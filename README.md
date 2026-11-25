# VAERS 2026 Exploratory Data Analysis (EDA) & Interactive Visualization

A comprehensive, reproducible exploratory data analysis and visualization project examining the Vaccine Adverse Event Reporting System (VAERS) 2026 dataset (**41,972 rows × 46 columns**).

> **Important Surveillance Note:** VAERS is a passive public health safety monitoring system. Reports reflect submitted observations and patterns in reporting rather than proven medical causation.

---

## Repository Contents

| File | Description |
| :--- | :--- |
| `VAERS_2026_EDA.ipynb` | Main Jupyter / Google Colab notebook containing 18 distinct EDA analyses, interactive Plotly visualizations, key findings, and health department recommendations. |
| `SRS_VAERS_2026_EDA-v2.docx` | Software Requirements Specification (SRS) detailing project scope, functional requirements (`FR-3.1`–`FR-4.4`), design constraints, and reproducibility standards. |
| `README.md` | Project overview, repository guide, and setup instructions. |

---

## Project Highlights & Methodology

### 1. Structured 18-Step Exploratory Data Analysis (Task 3)
To ensure thorough coverage without redundant outputs, all 18 core analyses examine distinct questions across three analytical levels:

* **Univariate Analysis (6 Steps — 3 Non-Visual, 3 Visual):** Age group distribution, patient sex share, IQR-capped onset interval (`NUMDAYS`) summary statistics, onset timing share (Pie Chart), continuous age distribution (Histogram with KDE), and symptom count spread (Box Plot).
* **Bivariate Analysis (6 Steps — 3 Non-Visual, 3 Visual):** Age group vs. onset timing cross-tabulation, age summary by sex, numeric correlation matrix, monthly report volume trend (Line Chart), age vs. capped onset days (Scatter Plot), and grouped age distributions across onset windows.
* **Multivariate Analysis (6 Steps — 3 Non-Visual, 3 Visual):** Mean capped `NUMDAYS` pivot across age group and sex, monthly counts by age group, grouped means by sex and onset timing, average symptom count across age and onset timing (Annotated Heatmap), monthly trends by onset timing (Multi-Line Chart), and a 3-variable colored scatter plot.

### 2. Interactive Plotly Visualizations
A dedicated interactive section built with `plotly.express` and `plotly.graph_objects` featuring:
* **Donut Chart & Area Chart** for interactive category and timeline exploration
* **Interactive Violin Plot** (`5,000`-row repeatable sample, `random_state=42`) comparing age density and quartiles by onset timing
* **Rotatable 3D Scatter Plot** (`5,000`-row repeatable sample, `random_state=42`) & **3D Surface Plot**

### 3. Key Findings & Health Department Recommendations (Task 4)
* **Most Reported Age Group:** `18-44 yrs` leads total submissions (**13,830 reports, 33.0%**), followed by `65+ yrs`.
* **Immediate Onset Dominance:** `Same day` onset accounts for **66.1%** of reports, underscoring the importance of prioritizing early-window intake checks.
* **Outlier-Resistant Reporting:** Extreme onset day values inflate raw averages, highlighting the value of pairing medians/IQRs with capped averages (`NUMDAYS` upper bound `2.50`) and maintaining natural category ordering.
* **Actionable Guidance:** Includes clear, plain-language recommendations tailored to public health surveillance teams.

---

## Tools & Libraries Used

* **Language:** Python 3.x
* **Data Manipulation:** `pandas`, `numpy`
* **Static Visualization:** `matplotlib`, `seaborn`
* **Interactive Visualization:** `plotly` (`plotly.express`, `plotly.graph_objects`)

---

## How to Run Locally or in Colab

1. Clone or download this repository:
   ```bash
   git clone [https://github.com/Rintu96/VAERS-2026-EDA.git](https://github.com/Rintu96/VAERS-2026-EDA.git)

2.Install required Python packages if running locally:
pip install pandas numpy matplotlib seaborn plotly jupyter
 

3.Open VAERS_2026_EDA.ipynb in Jupyter Notebook or Google Colab, ensure the cleaned dataset (df_clean) is available in your session, and run all cells top-to-bottom (Restart & Run All).

**Author:** Rintu Susan Reji

**Project:** Data Analytics & Visualization Project — VAERS 2026
