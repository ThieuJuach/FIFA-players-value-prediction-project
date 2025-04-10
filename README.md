Football Player Overall Rating Prediction

Welcome to the Football Player Rating Predictor — a data-driven machine learning pipeline designed to accurately predict a football player's overall rating based on their age, wage, market value, release clause, potential, and more.

This project leverages advanced regression techniques and feature selection to uncover the most impactful traits of top-tier players and build robust, explainable models.

Project Highlights

Data Preprocessing: Cleaned and combined numerical features with binary-encoded attributes to form a rich dataset for modeling.

Feature Selection: Reduced noise by selecting features with a strong correlation to overall (|corr| > 0.4), ensuring more accurate and interpretable models.

Model Training: Tuned and compared three powerful regressors using HalvingGridSearchCV:

Random Forest Regressor

XGBoost Regressor

Gradient Boosting Regressor

Evaluation: Achieved a test MAE as low as 0.668 using XGBoost — a strong indicator of real-world accuracy.

Feature Importance: Identified the top 5 predictors of player ratings:

release_clause_eur

value_eur

age

potential

wage_eur

Files Overview

rating_prediction_pipeline.py – Main script for data processing, training, and evaluation.

top_features_model.py – Streamlined version using only the 5 most influential features for performance and explainability.

How to Run

bash
Copy
Edit

# Install requirements
pip install -r requirements.txt

# Run the pipeline
python rating_prediction_pipeline.py

# Run the top-features optimized version
python top_features_model.py

Sample Output

less
Copy
Edit

XGBoost Best Test MAE: 0.668

Top 5 Features: ['release_clause_eur', 'value_eur', 'age', 'potential', 'wage_eur']

Note

While features like market value and wage are excellent predictors, keep in mind they might be influenced by the overall score itself — consider this if you're deploying the model for scouting or career simulations.

Inspiration

This project was inspired by a love for football and a curiosity for what really makes a great player great, beyond just what we see on the pitch.







You said:
Just use words. Do not use figures 


ChatGPT said:
Absolutely! Here's a vivid, words-only version of the README.md without any figures or code blocks:

⚽ Football Player Overall Rating Prediction
This project explores the power of machine learning in predicting a football player's overall rating using real-world data. Built with precision, each step—from data cleaning to model optimization—was crafted to ensure reliable and explainable results.

At its core, the pipeline combines a mix of numerical and binary-encoded features that truly capture what makes a footballer stand out. By focusing on the most influential attributes, the model delivers not only strong performance but also insights into the factors that shape a player's perceived quality.

🚀 What This Project Does
The full pipeline begins with raw data and transforms it into a refined dataset. It filters out noise by focusing only on features with a meaningful correlation to the player's overall rating. Using advanced machine learning algorithms like Random Forest, XGBoost, and Gradient Boosting, it trains and evaluates models to determine which one performs best.

The project doesn't just stop at good results—it dives deeper by identifying the most important features. These include a player’s release clause, market value, age, potential, and weekly wage. Together, they offer a clear view of what drives high player ratings in the football world.

🔍 Why It Matters
Understanding what influences a footballer's rating can be crucial for scouts, analysts, and even game developers. This project simplifies that process, offering a lean version of the model that uses only the five most impactful features. It trades complexity for clarity without sacrificing much performance.

🧠 What You’ll Learn
By studying this codebase, you’ll learn how to:

Clean and prepare football data for machine learning

Select relevant features based on correlation and importance

Train and fine-tune powerful regression models

Interpret feature contributions to model predictions

💭 Final Thoughts
This isn't just a prediction engine—it's a conversation starter for how data can reflect real-world talent. It proves that behind every high-rated player, there's a story hidden in numbers, waiting to be told.
