# FIFA World Cup EDA (1974–2022)

## Overview
An exploratory data analysis of FIFA World Cup matches spanning 1974 to 2022,
covering key stages including Group matches, Round of 16, Quarter-finals, Semi-finals,
and the championship Final. The goal was not just to produce charts, but to ask
meaningful football questions and let the data answer them.

> Note: This dataset covers 1974 onwards and does not represent complete all-time
> World Cup records. All findings should be interpreted within this scope.

## Dataset
- Source: Kaggle
- 43 matches, 38 features, covering 1974–2022
- Stages covered: Group, Round of 16, Quarter-final, Semi-final, Final
- Features include: goals, xG, possession, shots on target, fouls,
  cards, attendance, penalty shootout data, tournament format, host nations

## Tools
Python | Pandas | NumPy | Matplotlib | Seaborn

## Structure
- Phase 1 — Data understanding, cleaning, dtype fixes, and scope verification
- Phase 2 — Univariate analysis (goals, attendance, possession, fouls, cards)
- Phase 3 — Bivariate analysis (possession vs goals, shots vs goals, era trends, home vs away)
- Phase 4 — Domain questions (nation dominance across stages vs finals, shootout patterns)

## Key Findings
- Shots on target strongly predict goals (r=0.78) — possession does not (r=0.37)
- Finals have become significantly lower scoring across eras (16→24→32 team formats)
- Argentina leads all-stage appearances (12), wins (8), and championship final wins (3)
- Netherlands are the biggest heartbreak team — 8 appearances, 0 World Cup titles
- "Home advantage" reflects bracket seeding, not geography — only 5/43 matches
  had the literal host nation as the home side

## Key EDA Lessons
- Always verify what a column label means before interpreting it
- Structurally missing data should never be filled with 0 or the mean
- Pair histograms with boxplots — each reveals what the other hides
- Segment your data before drawing conclusions — aggregated numbers hide the best stories
- Small datasets (n=43) require cautious interpretation of any correlation

## How to Run
1. Clone the repository
2. Place the dataset CSV in the project folder
3. Open the notebook and run all cells
