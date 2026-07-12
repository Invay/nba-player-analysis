# NBA Player Performance Analysis

Statistical analysis of two decades of NBA player data, exploring whether height and nationality actually determine scoring success — and whether the "tall, American, started young" archetype holds up statistically.

## Questions

1. Can a shorter player still be a good scorer, statistically speaking?
2. Are American players genuinely better than non-American players, or is that a perception rather than a pattern in the data?
3. Is there a real age cutoff for entering the NBA?

## Data

- **NBA Players dataset** (Kaggle: `justinas/nba-players-data`) — player-season observations from ~1996–2022, including height, weight, nationality, and box-score stats.
- **NBA Rookies dataset** (Kaggle: `ignaciovinuales/nba-rookies-stay-longer-than-2-years`) — rookie-season stats and entry age, 1979–2020.

## Methods

- Descriptive statistics and distribution plots (height, points per game)
- 99% confidence interval for the proportion of high-scoring short players
- Linear regression of points per game on height
- Two-sample t-tests comparing USA vs. non-USA players across points, assists, rebounds, and true shooting %
- Rookie entry-age distribution analysis

## Key findings

- **Height isn't destiny.** About 1.8% of players under 190cm still average 25+ points per game (99% CI: 1.0%–2.7%). A simple regression even shows a slight *negative* relationship between height and scoring — taller players trend toward slightly fewer points per game, not more.
- **The "American players are better" assumption doesn't hold.** USA players only came out significantly ahead on assists. On scoring, rebounding, and shooting efficiency, there was no significant evidence they outperform non-USA players — despite outnumbering them roughly 5 to 1 in the league.
- **There's a real, narrow entry window.** Most players enter the NBA at 22–23 years old; the oldest rookie in the dataset debuted at 35.

## Run it yourself

```bash
pip install kagglehub pandas matplotlib seaborn scipy scikit-learn
python nba_analysis.py
```

Requires a free [Kaggle](https://www.kaggle.com) account for `kagglehub` to download the datasets automatically.

## Tools

Python, pandas, matplotlib, seaborn, SciPy, scikit-learn

## Author

Ivan Chibisov — Business Management (AI & Data Analytics), University of Buckingham
