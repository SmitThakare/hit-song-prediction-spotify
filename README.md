# Spotify Hit Prediction Analysis 🎵

[![Open in Kaggle](https://kaggle.com/static/images/open-in-kaggle.svg)](https://www.kaggle.com/code/rajg28/sportify-data-analysis)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

## 📌 Project Overview
Machine learning analysis of Spotify tracks to predict:
1. **Hit songs** (78.22% accuracy)
2. Audio features (Danceability R²=0.483, Energy R²=0.578)
3. Feature relationships through 15+ visualizations

**Dataset Source:**  
[Kaggle Notebook by rajg28](https://www.kaggle.com/code/rajg28/sportify-data-analysis) (File: `data.csv`)

## 🚀 Quick Start
```bash
git clone https://github.com/SmitThakare/hit-song-prediction-spotify.git
cd hit-song-prediction-spotify
pip install -r requirements.txt
jupyter notebook

📂 Repository Structure

hit-song-prediction/
├── data/
│   └── spotify_data.csv       # Original dataset
├── notebooks/
│   └── sportify_analysis.ipynb         # Complete analysis
├── .gitignore
├── requirements.txt
└── README.md

🛠️ Setup
1. Prerequisites
# Create conda environment (recommended)
conda create -n spotify python=3.8
conda activate spotify
2. Install Dependencies
pip install -r requirements.txt
3. Run Analysis
jupyter notebook notebooks/sportify_analysis.ipynb
🔍 Key Files Explained
File	Purpose
notebooks/sportify_analysis.ipynb	Data exploration, visualization, Predictions (78.22% accuracy)
data/raw/spotify_data.csv	Original dataset (Kaggle source)
📊 Results Summary
Model	Target	Metric	Score
Logistic Regression	Hit Prediction	Accuracy	0.7822
Linear Regression	Danceability	R²	0.4830
Linear Regression	Energy	R²	0.5780
Results Visualization

🧠 Key Learnings
Data Quality Matters

Outlier removal improved accuracy by 14.8%

Feature engineering boosted R² scores by ~18%

Critical Features



top_features = [
    'energy', 
    'danceability', 
    'speechiness',
    'loudness_valence'  # Engineered feature
]
Best Visualization Insights
![cad622ec-c34a-40f3-aad8-485e65af2880](https://github.com/user-attachments/assets/98b83364-8fa6-44b3-b0ab-6a0d905bd3a2)
![d0e39d3b-fee5-4ee5-85bc-9242e1a12051](https://github.com/user-attachments/assets/9585ba1c-f744-4e0d-91f4-2226bb32f401)
![1c48abeb-d2e6-45da-b890-c2fd47b1c1ef](https://github.com/user-attachments/assets/02b44885-3819-4749-a701-74504671bc71)
![2922e0dc-9173-4dc6-8e5f-7dc8df867401](https://github.com/user-attachments/assets/9a8d1190-3050-4b6b-8fb4-ac125b612512)


Coorelation Heatmap
![bbabfb76-7693-463a-aac6-e9a4318408cc](https://github.com/user-attachments/assets/0172a648-f702-4d1c-b3ef-8df9019f64bc)


🤝 How to Contribute
Fork the repository

Create a new branch (git checkout -b improve-feature)

Commit changes (git commit -am 'Add new feature')

Push to branch (git push origin improve-feature)

Open a Pull Request
