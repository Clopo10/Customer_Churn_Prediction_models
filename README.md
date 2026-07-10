# Customer Churn Prediction Models

Customer Churn Prediction Models is a small machine learning project for predicting whether a customer is likely to churn based on telecom-style customer, service, and billing features. The workflow is implemented in a Jupyter notebook and compares baseline and tuned classifiers, with a focus on practical churn classification metrics such as precision, recall, and F1 score.

## Project Overview

The main notebook, [deliverables/churn_prediction.ipynb](deliverables/churn_prediction.ipynb), covers:

1. Loading the cleaned, encoded dataset.
2. Training baseline Logistic Regression, Decision Tree, and Random Forest models.
3. Improving the models with hyperparameter tuning.
4. Comparing the final models using accuracy, precision, recall, and F1 score.
5. Visualizing model performance and feature importance.

The prepared dataset is stored in [data/cleaned_dataset.csv](data/cleaned_dataset.csv). It already includes encoded categorical features and engineered columns such as `OptionalServices`, `HighFriction`, and `LoyalMonthlyPayer`.

## Results

The notebook produced the following test-set comparison for the tuned models:

| Model               | Accuracy | Precision | Recall | F1 Score |
| ------------------- | -------: | --------: | -----: | -------: |
| Random Forest       |   0.7551 |    0.5266 | 0.7674 |   0.6246 |
| Logistic Regression |   0.7360 |    0.5017 | 0.7834 |   0.6117 |
| Decision Tree       |   0.7367 |    0.5026 | 0.7807 |   0.6115 |

The strongest tuned model by F1 score was Random Forest. The notebook also saves a summary comparison in [deliverables/model_comparison_table.csv](deliverables/model_comparison_table.csv).

## Repository Structure

```text
README.md
requirements.txt
data/
	cleaned_dataset.csv
deliverables/
	churn_prediction.ipynb
	model_comparison_table.csv
```

## Requirements

The project uses a Python data science stack with packages such as:

- pandas
- numpy
- scikit-learn
- matplotlib
- seaborn
- jupyter / notebook

Install everything with:

```bash
pip install -r requirements.txt
```

## How To Run

1. Create and activate a virtual environment.
2. Install dependencies from `requirements.txt`.
3. Open [deliverables/churn_prediction.ipynb](deliverables/churn_prediction.ipynb) in Jupyter or VS Code.
4. Run the notebook from top to bottom.

If you want to start a local notebook server, run:

```bash
jupyter notebook
```

Then open the notebook from the `deliverables` folder.

## Notes

- The project expects the cleaned dataset to remain at [data/cleaned_dataset.csv](data/cleaned_dataset.csv).
- Re-running the notebook will regenerate the comparison outputs shown in the deliverables folder.
