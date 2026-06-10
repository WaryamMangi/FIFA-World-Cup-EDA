# FIFA World Cup EDA (1974–2022)

## Overview
An exploratory data analysis of FIFA World Cup matches from 1974 to 2022,
covering key stages including Group matches, Quarter-finals, Semi-finals, and Finals.

## Dataset
- Source: Kaggle
- 43 matches, 38 features
- Covers match stats, team performance, attendance, and shootout data

## Tools
Python | Pandas | NumPy | Matplotlib | Seaborn

## Structure
- Phase 1 — Data understanding, cleaning, and type fixes
- Phase 2 — Univariate analysis (goals, attendance, possession, cards)
- Phase 3 — Bivariate analysis (possession vs goals, shots vs goals, era trends, home vs away)
- Phase 4 — Domain questions (nation dominance, shootout patterns)

## Key Findings
- Shots on target strongly predict goals (r=0.78) — possession does not (r=0.37)
- Finals have become significantly lower scoring across eras (16→24→32 team formats)
- Argentina dominates both across all stages and in championship finals
- Netherlands are statistically the biggest heartbreak team — wins throughout, never the title
- "Home advantage" in this dataset reflects bracket seeding, not geographic advantage

## How to Run
1. Clone the repository
2. Place the dataset CSV in the project folder
3. Open the notebook and run all cells
