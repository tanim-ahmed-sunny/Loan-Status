# Loan Status Prediction

A machine learning project that predicts whether a loan application will be approved using applicant and loan information.

## Project Structure

- `main.ipynb` - data exploration, preprocessing, model training, and evaluation
- `dataset.csv` - loan application dataset used by the notebook

## Approach

The notebook:

1. Loads the data from `dataset.csv` with pandas.
2. Removes rows containing missing values.
3. Converts the target `Loan_Status` from `N`/`Y` to `0`/`1`.
4. Converts categorical features into numeric values.
5. Separates the features from the target and removes `Loan_ID`.
6. Splits the data into training and test sets using a stratified split.
7. Trains a support vector machine classifier with a linear kernel.
8. Reports training and test accuracy.

## Dataset Features

The dataset includes applicant and loan details such as:

- Gender and marital status
- Number of dependents
- Education and self-employment status
- Applicant and co-applicant income
- Loan amount and loan term
- Credit history
- Property area
- Loan approval status

## Requirements

- Python 3.9 or later
- Jupyter Notebook or JupyterLab
- NumPy
- pandas
- seaborn
- scikit-learn

Install the dependencies with:

```bash
python -m pip install numpy pandas seaborn scikit-learn jupyter
```

## Run the Project

From this directory, start Jupyter:

```bash
jupyter notebook
```

Open `main.ipynb` and run the cells from top to bottom.

Alternatively, execute the notebook from the command line with:

```bash
jupyter nbconvert --to notebook --execute main.ipynb --output executed_main.ipynb
```

## Notes

- The notebook currently drops rows with missing values rather than imputing them.
- The test split uses 10% of the cleaned data and preserves the target class distribution.
- The reported accuracy can vary if the preprocessing or train/test split is changed.
