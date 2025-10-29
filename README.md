# Housing Price Prediction

This repository contains a Jupyter Notebook for predicting housing prices using machine learning.

Files:
- `Housing Price Prediction Using Machine Learning.ipynb` — main notebook with data exploration, preprocessing, model training and evaluation.
- `dataset/Mumbai House Prices.csv` — dataset used in the notebook.

Quick start
1. Open `Housing Price Prediction Using Machine Learning.ipynb` in Jupyter or VS Code.
2. Make sure you have the required Python environment (pandas, scikit-learn, matplotlib, seaborn, etc.).
3. Run the notebook cells in order.

Author
- Name: Md.Nurzaman 

License
This project is released under the MIT License. See the `LICENSE` file for details.

Notes
- Replace the author name above with your real name if you want the README to show your name.
- If you prefer a different license, tell me which one and I will update both `README.md` and `LICENSE` accordingly.

## Analysis steps included in this project

The notebook `Housing Price Prediction Using Machine Learning.ipynb` walks through the following steps. You can use this as a checklist while running the notebook locally.

1. Load Dataset
	- Load the Kaggle dataset (6,348 property listings) from `dataset/Mumbai House Prices.csv`.
	- Inspect the data using `df.head()`, `df.info()` and `df.shape`.

2. Data Cleaning
	- Handle missing values (`dropna()` or imputation), remove duplicates (`df.drop_duplicates()`), and detect/cap outliers (for example using price-per-sqft quantiles or z-score filtering).

3. Convert Nominal Data
	- Encode categorical features (e.g., `Location`, `New/Resale`) numerically using label encoding or one-hot encoding depending on the algorithm and cardinality.

4. Correlation Heatmap
	- Compute correlations for numeric features and visualize them with a heatmap (Seaborn `heatmap`) to identify strongly related predictors.

5. Train Models (Linear Regression + Gradient Descent)
	- Train a standard Linear Regression model (scikit-learn) and also implement an explicit Gradient Descent fit (for learning/experimentation).
	- Keep the selected features and show model coefficients.

6. Test Accuracy (Scatterplots)
	- Plot predicted vs actual values using scatterplots for both models and include the perfect-prediction line for visual comparison.

7. Evaluate Models (R²)
	- Calculate the coefficient of determination (R²) for each model using `sklearn.metrics.r2_score` and report explained/unexplained variance.

How to run
- Open `Housing Price Prediction Using Machine Learning.ipynb` in VS Code or Jupyter Notebook.
- Ensure required packages are installed (typical packages: pandas, numpy, matplotlib, seaborn, scikit-learn). You can create a virtual environment and install dependencies.

Example (PowerShell):

```powershell
python -m venv .venv; .\.venv\Scripts\Activate.ps1
pip install pandas numpy matplotlib seaborn scikit-learn
```

Then open the notebook and run the cells in order. The notebook already contains cells for loading the local `dataset/Mumbai House Prices.csv`, preprocessing, encoding, visualization, training, and evaluation.
