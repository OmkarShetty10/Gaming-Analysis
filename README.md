🎮 Online Gaming Player Engagement Analysis
1. Overview

This project analyzes a rich dataset of online gaming players to understand and predict engagement levels.
It combines player demographics (age, gender, location) with in-game activity (game genre, difficulty, level, achievements, playtime, session frequency, purchases, etc.) to uncover what drives higher engagement.

Goal:
Predict each player’s engagement level (High, Medium, Low) and identify key behavioral factors influencing it.
Insights from this analysis are intended to help game designers and marketers enhance player retention and tailor experiences (e.g., targeted rewards or challenges) to boost engagement and loyalty.

2. Dataset Description

2.1. Dataset Size and Structure

Size: 40,034 player records

Columns: 13 (features + target)

2.2. Key Features

Demographics:

Age

Gender

Location

Game Attributes:

GameGenre

GameDifficulty

PlayerLevel

AchievementsUnlocked

Engagement Metrics:

PlayTimeHours — average hours per session

SessionsPerWeek — frequency of gaming

AvgSessionDurationMinutes — average time per session

InGamePurchases — binary (0 = No, 1 = Yes)

Target Variable:

EngagementLevel — categorical (High, Medium, Low)

2.3. Data Quality

No missing values

Mix of numerical and categorical fields

Clean and sizable dataset for robust statistical and ML analysis

3. Exploratory Data Analysis (EDA)

3.1. Age Distribution

Mostly young adults (20–40 years)

Median age: ~32

Peak range: 25–30 years

3.2. PlayTimeHours

Most players: 10–15 hours per session

Small group: 20–24 hours (hardcore gamers)

3.3. InGamePurchases

80% of players: no purchases (0)

20% of players: make purchases (1)

3.4. SessionsPerWeek

Most players: 5–10 sessions per week

Some highly active players: up to 19 sessions

3.5. AvgSessionDurationMinutes

Roughly normal distribution (centered ~90–100 minutes)

Middle 50%: 50–150 minutes per session

3.6. PlayerLevel

Uniform spread from 1 to 99

Indicates smooth progression without major bottlenecks

3.7. AchievementsUnlocked

Majority: 15–30 achievements unlocked

Fewer players exceed 30 achievements

4. Correlation Insights
Feature	Correlation (≈)	Interpretation
SessionsPerWeek	0.606	Strong positive — frequent sessions correlate with higher engagement
AvgSessionDurationMinutes	0.477	Moderate positive — longer sessions → more engaged players
AchievementsUnlocked	0.061	Weak positive — small association with engagement
PlayerLevel	0.059	Weak positive — higher levels slightly more engaged
Other Features (Age, Gender, etc.)	~0	Negligible correlation individually
5. Tools & Libraries Used

5.1. Environment

Python 3.x

Jupyter Notebook

5.2. Libraries

Data Manipulation: pandas, numpy

Visualization: matplotlib, seaborn

Machine Learning: scikit-learn, LightGBM, CatBoost

Utilities: IPython.display, warnings

6. Key Takeaways

Session Frequency Matters:

Players logging in 5+ times/week are significantly more engaged.

Implement daily login rewards, streak bonuses, or push notifications to increase retention.

Longer Sessions Correlate with Engagement:

Sessions lasting 1–2 hours show higher engagement.

Design longer missions, story arcs, or immersive gameplay loops to encourage sustained play.

Achievements and Progression Add Value:

Weak but positive impact on engagement.

Highlight level milestones and achievement rewards to complement other strategies.

Target Core Demographic:

Majority of players: young adults (20s–30s).

Tailor marketing campaigns and social features toward this audience.

Monetization Insight:

Only ~20% make purchases (consistent with freemium model).

Focus on converting mid/high engagement players into paying users through targeted offers.

Holistic Engagement:

Engagement results from combined behavioral factors, not isolated demographics.

7. Future Work

Predictive Modeling:

Develop classification models (Random Forest, LightGBM, CatBoost).

Evaluate accuracy and feature importance for interpretability.

Player Segmentation:

Apply clustering to identify player personas (e.g., casual vs. hardcore).

A/B Testing Strategies:

Test different reward schedules or engagement incentives.

Measure impact on player activity and retention.

Rich Behavioral Data Integration:

Include time-series logs of in-game activity (e.g., level-ups, social actions).

Use survival analysis or churn prediction models.

Personalization & Gamification:

Develop recommender systems for challenges or missions.

Implement leaderboards, badges, and personalized notifications.

8. How to Run

8.1. Setup

Install Python 3.x and Jupyter Notebook (Anaconda recommended).

8.2. Install Dependencies

pip install pandas numpy matplotlib seaborn scikit-learn lightgbm catboost


8.3. Obtain Dataset

Place the dataset file:
online_gaming_behavior_dataset.csv
in the working directory, or update the file path in the notebook.

8.4. Run the Notebook

jupyter notebook


Open gaming-analysis.ipynb

Execute all cells sequentially to reproduce analysis

8.5. Environment Notes

Compatible with Python 3.x

No GPU required

Works on standard hardware setups
