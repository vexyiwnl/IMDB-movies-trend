# IMDB Movies — Data Science Project

A data science project that analyzes IMDB movie data to predict ratings, classify hits vs flops, and uncover trends in film performance.

## Business Problem

- **Can we predict a movie's rating or revenue** based on features like genre, duration, votes, and box office gross?
- **Can we classify movies as hit or flop** (e.g., rating ≥ 7.0)?

## Objectives

1. Clean and preprocess data  
2. Exploratory Data Analysis (EDA)  
3. Build predictive models (Linear & Logistic Regression)  
4. Prepare data for Power BI / Tableau dashboards  

## Project Structure

```
IMDB movies trend/
├── imdb_movies.csv          # Raw dataset
├── IMDB_Movies_DataScience.ipynb  # Main analysis notebook
├── IMDB_cleaned.csv         # Preprocessed data (generated)
├── requirements.txt         # Python dependencies
└── README.md
```

## Dataset

The dataset (`imdb_movies.csv`) contains ~1,000 movies with the following columns:

| Column | Description |
|--------|-------------|
| movie_id | Unique identifier |
| title | Movie title |
| year | Release year |
| certificate | Age rating (G, PG, PG-13, R) |
| runtime_minutes | Duration in minutes |
| genre | Genre(s), comma-separated |
| rating | IMDB rating (1–10) |
| metascore | Metacritic score |
| votes | Number of IMDB votes |
| gross_millions | Box office gross (millions USD) |

## Setup

1. **Clone the repository** (or navigate to the project folder)

2. **Create a virtual environment** (recommended):
   ```bash
   python -m venv venv
   venv\Scripts\activate   # Windows
   # or: source venv/bin/activate   # macOS/Linux
   ```

3. **Install dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

4. **Run the notebook**:
   ```bash
   jupyter notebook IMDB_Movies_DataScience.ipynb
   ```
   Or open in VS Code and run all cells.

## Workflow

1. **Load & Inspect** — Load data, check `info()`, `describe()`, missing values, duplicates  
2. **Preprocessing** — Handle missing values, convert types, feature engineering (movie age, genre count, hit/flop target), encode categoricals  
3. **EDA** — Rating distribution, genre vs rating, gross vs rating, trends over years, hit vs flop pie  
4. **Models** — Linear Regression (predict rating), Logistic Regression (classify hit/flop)  
5. **Export** — Save `IMDB_cleaned.csv` for dashboards  

## Outputs

- **IMDB_cleaned.csv** — Preprocessed data ready for Power BI or Tableau  
- **Visualizations** — Histograms, bar charts, scatter plots, line charts, pie chart  
- **Model metrics** — RMSE, R² (regression); Accuracy, Precision, Recall (classification)  

## Dashboard Recommendations (Power BI / Tableau)

| Insight | Chart Type |
|---------|------------|
| Rating trend over years | Line Chart |
| Genre vs Avg Rating | Bar Chart |
| Hit vs Flop counts | Pie / Donut Chart |
| Genre & Certificate | Heatmap |
| Predictions vs Actual | Scatter Plot |

## Dependencies

- pandas  
- numpy  
- matplotlib  
- seaborn  
- scikit-learn  
- jupyter  

## License

MIT
