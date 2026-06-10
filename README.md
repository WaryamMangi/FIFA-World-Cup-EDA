IFA World Cup EDA (1974–2022)
Overview
This project is a structured Exploratory Data Analysis of FIFA World Cup matches spanning 1974 to 2022. It covers key tournament stages — Group matches, Round of 16, Quarter-finals, Semi-finals, and the championship Final — and works through four progressive phases: data understanding, univariate analysis, bivariate analysis, and domain-specific questions.
The goal was not just to produce charts, but to ask meaningful football questions and let the data answer them.

Dataset

Source: Kaggle
Scope: 43 matches, 38 features, covering 1974–2022
Stages covered: Group, Round of 16, Quarter-final, Semi-final, Final
Key features: Goals, xG, possession, shots on target, fouls, cards, attendance, penalty shootout data, tournament format, host nations


Note: This dataset does not represent complete all-time World Cup records. Matches before 1974 are not included — Brazil's 1958, 1962, and 1970 titles fall outside the dataset's range. All findings should be interpreted within this scope.


Tools & Libraries
Python | Pandas | NumPy | Matplotlib | Seaborn

Project Structure
├── fifa_worldcup_eda.ipynb     # Main Jupyter Notebook
├── fifa_worldcup.csv           # Raw dataset
└── README.md

Analysis Structure
Phase 1 — Data Understanding & Cleaning

Audited shape, dtypes, and missing values
Converted date from string to datetime64
Recategorized tournament_format (16, 24, 32) into era labels
Identified penalty_home / penalty_away as structurally missing — NaN means no shootout occurred, not corrupted data
Verified dataset scope: 13 actual championship finals out of 43 total matches

Phase 2 — Univariate Analysis

Goal distributions: home, away, and total goals — all right-skewed with early-era outliers
Attendance: bimodal distribution reflecting smaller stadiums in early eras vs modern venues
Possession: home teams consistently control more of the ball; home and away possession are perfectly complementary (sum to 100%)
Fouls and cards: away teams commit more fouls and receive more yellow cards on average

Phase 3 — Bivariate Analysis

Possession vs Goals: Weak correlation for both home (r=0.37) and away (r=0.27) sides — possession alone is a poor predictor of goals
Shots on Target vs Goals: Strong correlation for home (r=0.78) and moderate-to-strong for away (r=0.68) — a significantly better predictor than possession
Scoring Trends Across Eras: Finals have become progressively lower-scoring from the 16-team era (median ~3.5 goals) to the 32-team era (median ~2.5 goals), reflecting global tactical evolution
Home vs Away Performance: Home teams won 32 matches vs 9 for away teams — but only 5 of 43 matches had the literal host nation as home. The disparity reflects bracket seeding, not geographic advantage

Phase 4 — Domain Questions

Nation Dominance: Argentina leads both all-stage appearances (12) and wins (8), and championship final wins (3). The Netherlands are statistically the biggest heartbreak team — 8 appearances and 4 stage wins, yet 0 championship final victories
Penalty Shootouts: Filtered to 9 confirmed shootout matches (excluding AET matches decided before penalties). Home sides score slightly more penalties on average (3.5 vs 2.9)


Key Findings
QuestionFindingDoes possession predict goals?No — correlation of 0.37 (home) and 0.27 (away), both weakDo shots on target predict goals?Yes — correlation of 0.78 (home) and 0.68 (away), both strongAre finals becoming more or less attacking?Less — median goals dropped from 3.5 to 2.5 across erasIs home advantage real?No — "home" is a bracket label, not geographic; only 5/43 matches had the literal host nation as home teamWhich nation dominates?Argentina — leads appearances, stage wins, and championship final winsBiggest heartbreak team?Netherlands — 8 appearances, 0 World Cup titles

Key EDA Lessons Documented

Always verify what a column label actually means before interpreting it
Pair histograms with boxplots for continuous variables — each reveals what the other hides
Structurally missing data (like penalty NaNs) should never be filled with 0 or the mean
Numeric-looking columns are not always numeric — tournament_format encoded categorical eras
Segment your data before drawing conclusions — aggregated numbers hide the most interesting stories
Small datasets (n=43) require cautious interpretation — weak correlations may be noise


How to Run

Clone this repository
Place fifa_worldcup.csv in the project folder
Open fifa_worldcup_eda.ipynb in Jupyter
Run all cells from top to bottom
