# Spotify Hit Prediction Analysis 🎵

[![Open in Kaggle](https://kaggle.com/static/images/open-in-kaggle.svg)](https://www.kaggle.com/code/rajg28/sportify-data-analysis)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

## Project Overview
This machine learning project analyzes Spotify song data to:
- Predict song popularity (hit vs. non-hit)
- Model audio features (danceability, loudness, energy)
- Explore feature relationships through visualization

**Key Results:**
- 🎯 Hit Prediction Accuracy: 78.22%
- 💃 Danceability R²: 0.4830
- 🔊 Loudness R²: 0.4308
- ⚡ Energy R²: 0.5780

## Dataset Information
**Source:** [Kaggle Dataset](https://www.kaggle.com/code/rajg28/sportify-data-analysis) (File: `data.csv`)

### Feature Descriptions
```
| Feature | Description | Range |
|---------|-------------|-------|
| `acousticness` | Confidence measure of acoustic content | 0-1 |
| `danceability` | Suitability for dancing | 0-1 |
| `energy` | Intensity measure | 0-1 |
| `loudness` | Overall loudness in dB | -60-0 |
| `valence` | Musical positivity | 0-1 |
| `target` | Hit classification label | 0-1 |
```
### 📂 Repository Structure
```
hit-song-prediction/
├── data/
│   └── spotify_data.csv       # Original dataset
├── notebooks/
│   └── sportify_analysis.ipynb # Complete analysis
├── .gitignore
├── requirements.txt
└── README.md
```

### Key Learnings
## Data Processing
Improved accuracy from 63.39% → 78.22% through:

Outlier removal (IQR method)

Feature engineering (19 new features)

Stratified sampling (60:40 class balance)

## Feature Engineering
# Sample engineered features
```
df['danceability_energy'] = df['danceability'] * df['energy']
df['log_tempo'] = np.log1p(df['tempo'])
df['energy_squared'] = df['energy']**2
```
# Model Performance
Model	Target	Metric	Score
Logistic Regression	Hit Prediction	Accuracy	0.7822
Linear Regression	Danceability	R²	0.4830
Linear Regression	Energy	R²	0.5780

### Visualizations
## Correlation Heatmap
![bbabfb76-7693-463a-aac6-e9a4318408cc](https://github.com/user-attachments/assets/cc720d37-e481-4b3b-9f73-3bad65cf83d5)

## Feature Distributions
![1c48abeb-d2e6-45da-b890-c2fd47b1c1ef](https://github.com/user-attachments/assets/80989320-4de3-4bdc-bfd7-466d7e003e0b)


### Requirements
pandas>=1.3.0
numpy>=1.21.0
matplotlib>=3.4.0
seaborn>=0.11.0
scikit-learn>=0.24.0
statsmodels>=0.12.0
jupyter>=1.0.0

### Future Improvements
Experiment with ensemble methods (Random Forest/XGBoost)

Add hyperparameter tuning

Incorporate lyrics analysis

Build Streamlit dashboard



## 🚀 Quick Start
# Clone repository
```
git clone https://github.com/SmitThakare/hit-song-prediction-spotify.git
cd hit-song-prediction-spotify
```

# Create environment (recommended)
```
conda create -n spotify python=3.8
conda activate spotify
```
# Install dependencies
```
pip install -r requirements.txt
```
# Run analysis
```
jupyter notebook notebooks/sportify_analysis.ipynb
```
### 🤝 How to Contribute
Fork the repository

Create your feature branch (git checkout -b new-feature)

Commit changes (git commit -am 'Add feature')

Push to branch (git push origin new-feature)

Open a Pull Request

📜 License: MIT

