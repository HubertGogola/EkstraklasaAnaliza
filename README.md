# Ekstraklasa Data Analysis

This project analyzes match data from the **Polish Ekstraklasa** (top football league in Poland) using Python and Jupyter Notebooks.  
The dataset (`POL.xlsx`) contains match-level data such as teams, goals, results, dates, and betting odds.  
The analysis produces summary statistics, visualizations, and reports.

---

## 📂 Project Structure

- `projekt.ipynb` — main Jupyter Notebook with all code, analysis, and visualizations.  
- `POL.xlsx` — raw dataset with match results and betting odds.  
- `figures/` — folder with all generated plots (PNG).  
- `exports/` — folder with exported CSV tables and results.  
- `report.md` / `report.html` — auto-generated report with insights and plots.  
- `ekstraklasa_extras.py` — extra functions for Elo ratings, Poisson model, head-to-head heatmaps, and rolling form.

---

## ⚽ Data Description

Each row in `POL.xlsx` represents a single match and typically includes:

- `Date` — match date  
- `Season` — season (e.g. 2021/2022)  
- `HomeTeam`, `AwayTeam` — team names  
- `FTHG`, `FTAG` — full-time home and away goals  
- `FTR` — full-time result (`H`, `D`, `A`)  
- `PSCH`, `PSCD`, `PSCA` — betting odds for home, draw, away  

Derived variables:
- `TotalGoals` = `FTHG + FTAG`  
- Probabilities implied from odds (`pH`, `pD`, `pA`)  

---

## 📊 Analyses & Visualizations

The notebook generates multiple insights and plots:

1. **Average goals per season** — line chart.  
2. **Match outcomes (H/D/A) shares per season** — bar chart.  
3. **Histogram of total match goals** — goal distribution.  
4. **Over 1.5 / Over 2.5 goals trend** — seasonal proportions.  
5. **Points table and title race** — cumulative points race for top 4 teams.  
6. **Home vs Away goals by team** — grouped bar chart.  
7. **Kickoff time distribution** — most common match hours.  
8. **Rolling team form** — moving averages of points and goals.  
9. **Elo ratings** — rating progression over time for selected teams.  
10. **Head-to-Head heatmaps** — goal differences between teams in a season.  
11. **Betting odds calibration** — reliability plots for H/D/A outcomes.  
12. **Scatter: implied p(H) vs goal difference** — how well odds reflect match dominance.

---

## 📈 Methods

- **Descriptive statistics** with `pandas`  
- **Visualizations** with `matplotlib`  
- **Elo rating system** for team strength over time  
- **Poisson model** for expected goals and win/draw probabilities  
- **Betting market calibration** via Brier score and calibration plots  

---

## 🚀 How to Run

1. Install required Python libraries:
   ```bash
   pip install pandas numpy matplotlib openpyxl
