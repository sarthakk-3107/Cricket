🏏 Cricket Win Probability Prediction Using Machine Learning
Predicting win probability during an ODI cricket match using real ball-by-ball data and ML models like XGBoost and LightGBM.

📌 Project Motivation
"What are the chances of winning from here?"
A question that arises in every nail-biting cricket match. This project aims to answer it using real match data and machine learning — not just intuition.

🧠 ML Workflow

✅ Step 1: Data Collection
Parsed 20+ raw JSON files containing ball-by-ball data from actual ODI matches.
Converted data into structured CSV format with match context (venue, inning, over, batter, bowler, etc.)


✅ Step 2: Feature Engineering
Created match-state features such as:
balls_remaining, runs_remaining
current_run_rate, required_run_rate
run_rate_diff, wickets_remaining


✅ Step 3: Labeling
Each row (ball) is labeled based on the final outcome:
1 for Win, 0 for Loss
The task becomes a binary classification problem.


✅ Step 4: Model Training
Trained two popular tree-based models:
Model	Accuracy	ROC AUC	Notes
XGBoost	99.17%	0.9989	Slightly better metrics
LightGBM	98.84%	0.9938	Faster training, efficient
Applied GridSearchCV on XGBoost for hyperparameter tuning.
Evaluated using confusion matrix, classification report, and AUC score.


📊 Visual Comparison
Included visual bar charts to compare:
Accuracy between XGBoost and LightGBM
ROC AUC scores
Training performance and generalization


🔭 Next Steps
📌 Include contextual features:
🪙 Toss result
🏏 Pitch and venue conditions
🌍 Generalize pitch types by country
🧠 Try sequence modeling with LSTM or Transformers
📈 Visualize in-match win probability over time
