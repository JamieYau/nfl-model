# NFL Prediction Model

This model predicts the Total points spread Over/Under for NFL games using a K-Nearest Neighbors classifier.

## Overview

The model uses historical NFL game data to predict whether the total points scored in a game will go over or under the bookmakers' line.

## Data

- Source: [Pro-Football-Reference](https://www.pro-football-reference.com/)
- Years covered: 2015-2024
- Features used:
  - Spread: The betting spread for the game
  - Total: The over/under line set by bookmakers
- Target variable: Under (1 if actual total was under the line, 0 if over)

## Model

- Algorithm: K-Nearest Neighbors classifier
- Parameters:
  - n_neighbors: 7
  - Features are standardized using StandardScaler
  - Outlier detection using LocalOutlierFactor

### Model Performance

#### Current Model (v1.0)

- Overall Performance by season:
  - 2021: 49.62%
  - 2022: 53.41%
  - 2023: 59.92%

- Performance on Unders:
  - 2021: 52.85%
  - 2022: 58.77%
  - 2023: 63.12%

## Project Structure

```bash
├── data/
│   ├── nfl_gamelog_2015-2024.csv
├── notebooks/
│   ├── data_scraping.ipynb
│   ├── nfl_model.ipynb
├── README.md
└── ...
```

## Setup

1. Clone the repository
```bash
git clone https://github.com/your-username/nfl-model.git
cd nfl-model
```

2. Create and activate virtual environment:
```bash
python -m venv pyenv
source pyenv/bin/activate
```

3. Install dependencies:
```bash
pip install -r requirements.txt
```

4. Run the notebooks to scrape data and train the model
```bash
jupyter notebook notebooks/data_scraping.ipynb
jupyter notebook notebooks/nfl_model.ipynb
```

## Improvements

- [x] Remove Novelty Data
- [x] Add scaling
- [ ] Add more features
- [ ] Experiment with different algorithms
- [ ] Implement cross-validation
- [ ] Add web scraping for automated data updates
- [ ] Deploy model as API
- [ ] Create a web interface for predictions

## License

This project is open-sourced under the MIT License - see the `LICENSE` file for details.
