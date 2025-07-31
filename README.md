# 🏠 Gurgaon Housing Price Prediction

A complete machine learning pipeline for predicting median house values in Gurgaon using Python and Scikit-Learn. This project includes data preprocessing, feature engineering, training a Random Forest model, and generating predictions with visualization.

## 📌 Features

- End-to-end ML workflow: Load → Clean → Train → Predict
- Stratified sampling based on income
- Model and pipeline saved using `joblib` for future inference
- Generates predictions and saves to `Output.csv`
- Visualizes actual vs predicted values

## 🔧 Tech Stack

- Python
- Pandas, NumPy, Matplotlib, Seaborn
- Scikit-Learn (RandomForestRegressor, Pipelines)
- Joblib for model persistence

## 📂 Project Structure
<pre>
gurgaon-housing-price-prediction/
├── main.py                   # Core script for training and inference
├── housing.csv               # Dataset with housing features
├── Output.csv                # Generated predictions
├── actual_vs_predicted.png   # Scatter plot showing model performance
├── requirements.txt          # Python dependencies
├── README.md                 # Project documentation
├── .gitignore                # Ignored files and folders
</pre>


## ▶️ How to Run

1. Clone the repo:
   ```bash
   git clone https://github.com/namanj04/gurgaon-housing-price-prediction.git
   cd gurgaon-housing-price-prediction
   ```
2. Install Dependencies
   ```bash
   pip install -r requirements.txt
   ```
3. Run the Script
   ```bash
   python main.py
  
4. After Running

- If `model.pkl` does **not** exist:
  - The script will perform data preprocessing
  - Train a `RandomForestRegressor` model
  - Save both the model and pipeline using `joblib`

- If `model.pkl` **already exists**:
  - The script will load the saved model and pipeline
  - Perform inference on `input.csv` (generated from test split)
  - Save the predictions to `Output.csv`

## 📈 Visualization
### 📊 Sample Output

| longitude | latitude | housing_median_age | total_rooms | ocean_proximity | actual_value              | predicted_value           |
|-----------|----------|--------------------|-------------|------------------|--------------------------|----------------------|
| 77.10     | 28.42    | 15                 | 520         | NEAR_OCEAN       | 289000.0                 | 284752.4             |
| 77.02     | 28.48    | 18                 | 640         | INLAND           | 245000.0                 | 249103.1             |
| 77.15     | 28.39    | 12                 | 710         | NEAR_BAY         | 325000.0                 | 318671.6             |

## 🔄 Future Improvements

- Add evaluation metrics like RMSE, MAE, and R² to assess model performance
- Integrate hyperparameter tuning using GridSearchCV or RandomizedSearchCV
- Convert the script into a Jupyter Notebook for better exploration
- Build a simple web UI using Streamlit or Flask for interactive predictions
- Deploy the model via Render or HuggingFace Spaces for public access
- Add logging and exception handling for robustness
- Improve feature engineering with domain knowledge

---

**👨‍💻 Built by [Naman Jain](https://www.linkedin.com/in/namanj04)**  
📌 Open for collaboration and feedback!



