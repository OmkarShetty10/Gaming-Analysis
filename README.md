🎮 Online Gaming Player Engagement Analysis
🧩 Overview

This project analyzes a rich dataset of online gaming players to understand and predict engagement levels.
It combines player demographics (age, gender, location) with in-game activity (genre, difficulty, level, achievements, playtime, session frequency, purchases, etc.) to uncover what drives higher engagement.

Goal:
Predict each player’s engagement level (High, Medium, Low) and identify key behavioral factors influencing it.
Insights from this analysis help game designers and marketers enhance player retention and tailor experiences (e.g., targeted rewards or challenges) to boost engagement and loyalty.

📊 Dataset Description

Size: 40,034 player records

Columns: 13 (features + target)

Key Features:

Demographics: Age, Gender, Location

Game Attributes: GameGenre, GameDifficulty, PlayerLevel, AchievementsUnlocked

Engagement Metrics:

PlayTimeHours (avg hours per session)

SessionsPerWeek

AvgSessionDurationMinutes

InGamePurchases (0 = no, 1 = yes)

Target: EngagementLevel (High, Medium, Low)

Data Quality:
✅ No missing values
✅ Mix of numerical and categorical fields
✅ Clean and sizable — supports robust statistical and ML analysis

🔍 Exploratory Data Analysis (EDA)
📈 Key Insights

Age: Mostly young adults (20–40 years). Median ≈ 32. Peak between 25–30.

PlayTimeHours: Clustered around 10–15 hours per session. Small hardcore segment (~20–24 hrs).

InGamePurchases: ~80% don’t purchase, ~20% do — typical freemium model.

SessionsPerWeek: Common range: 5–10 sessions. Long tail up to 19 sessions.

AvgSessionDurationMinutes: Roughly normal around 90–100 minutes (IQR: 50–150).

PlayerLevel: Uniform distribution (1–99) — steady progression.

AchievementsUnlocked: Most players: 15–30 achievements. Fewer exceed 30.

📈 Correlation Insights
Feature	Correlation (≈)	Interpretation
SessionsPerWeek	0.606	Strong positive — frequent players are more engaged.
AvgSessionDurationMinutes	0.477	Moderate positive — longer sessions mean higher engagement.
AchievementsUnlocked	0.061	Weak positive — slight engagement link.
PlayerLevel	0.059	Weak positive — higher levels = modestly more engaged.
Others (Age, Gender, etc.)	~0	Minimal direct correlation — engagement depends on behavior patterns, not demographics.
🧠 Tools & Libraries Used

Environment: Python 3.x, Jupyter Notebook

Data Manipulation: pandas, numpy

Visualization: matplotlib, seaborn

Machine Learning: scikit-learn, LightGBM, CatBoost

Utilities: IPython.display, warnings

🚀 Key Takeaways

Session Frequency Matters:
Players with 5+ sessions/week are substantially more engaged.
→ Use daily login rewards, streak bonuses, or push notifications to encourage consistent play.

Lengthy Sessions Support Engagement:
Longer average sessions (1–2 hours) correlate with deeper engagement.
→ Create immersive content (missions, story arcs, extended challenges).

Achievements & Progression Help:
Correlations are weak but complement retention.
→ Reward milestones and highlight progress — combine with other engagement systems.

Target Core Demographic:
Majority are young adults (20–30s).
→ Focus marketing, features, and aesthetics toward this segment (social/competitive modes).

Monetization Insight:
~20% of players make purchases — aligns with the “power user” revenue pattern.
→ Offer personalized deals or VIP perks for high-engagement users.

Holistic Engagement:
No single factor predicts engagement — success comes from a blend of play frequency, session duration, and rewarding progression.

🧩 Future Work

Predictive Modeling:

Build ML models (Random Forest, LightGBM, CatBoost) to classify engagement level.

Use feature importance for interpretability.

Player Segmentation:

Apply clustering (e.g., K-Means, DBSCAN) to identify personas like “casual vs hardcore”.

A/B Testing:

Experiment with reward schedules, missions, or notifications.

Measure engagement changes statistically.

Rich Behavioral Data:

Add time-series data (sessions over weeks, level progression).

Explore player churn and lifetime value modeling.

Personalization & Gamification:

Build recommender systems for challenges, items, or modes.

Use leaderboards, badges, and social incentives to enhance retention.

⚙️ How to Run
1️⃣ Setup

Install Python 3.x and Jupyter Notebook (Anaconda recommended).

2️⃣ Install Dependencies
pip install pandas numpy matplotlib seaborn scikit-learn lightgbm catboost

3️⃣ Obtain Dataset

Place the dataset file:
online_gaming_behavior_dataset.csv
in the working directory (or update the file path in the notebook).

4️⃣ Run the Notebook
jupyter notebook


Open gaming-analysis.ipynb and execute all cells sequentially.

5️⃣ Environment Notes

Works on standard CPU — no GPU required.

Tested on Python 3.x with stable library versions.
