# Handwriting_Digits_Jupyter
Predictive models using the digits dataset from sklearn. <br> 
The following image is an example plotted data point representing a hand written number<br>
![image](https://github.com/FireEden/Handwriting_Digits_Jupyter/assets/38669490/758a128a-bbe8-42f6-ab16-b15e78011a86)

# Handwritten Digit Recognition

A machine learning project that classifies images of handwritten digits (0–9) and compares several classification models using cross-validation.

This project uses **scikit-learn** and its built-in `digits` dataset. Rather than focusing on a single model, it walks through training multiple models, comparing their accuracy, and demonstrating different cross-validation techniques to evaluate them fairly.

## What it does

Each image in the dataset is an 8×8 grayscale picture of a handwritten digit. The project:

1. Loads and explores the digits dataset.
2. Trains several models to recognize which digit (0–9) an image shows.
3. Compares the models' accuracy using K-Fold and Stratified K-Fold cross-validation.
4. Tunes model settings (like the number of trees in the Random Forest) to see how performance changes.

## The dataset

The project uses scikit-learn's built-in **digits** dataset (`load_digits`):

- 1,797 images of handwritten digits.
- Each image is **8×8 pixels** (64 values total), in grayscale.
- Each image is labelled with the digit it represents (0 through 9).

Because the dataset is built into scikit-learn, there's no separate file to download — it loads automatically when you run the code.

## Models compared

The project trains and compares three classification models:

| Model | Notes |
|---|---|
| Logistic Regression | `max_iter = 10000` |
| Support Vector Machine (SVC) | default settings |
| Random Forest | tested with different numbers of trees (15, 40, 50, 100) |

## Cross-validation techniques demonstrated

A key part of this project is showing different ways to evaluate a model reliably, rather than trusting a single train/test split:

- **Train/test split** — a simple single split of the data.
- **K-Fold** — splits the data into chunks ("folds") and tests on each one in turn. Shown both as a manual `for` loop (to illustrate the concept) and with the simpler `cross_val_score` function.
- **Stratified K-Fold** — like K-Fold, but keeps each digit evenly represented across folds.
- **Repeated Stratified K-Fold** — repeats the stratified process multiple times for a more stable estimate, reporting the mean score and standard deviation.

## Files

- `Digits_Handwriting_Model_Jupyter.ipynb` — the full notebook with data exploration, model training, and cross-validation comparisons.

## Getting started

If you're new to this, here's how to run it.

1. Make sure you have Python installed.
2. Install the required libraries:

```bash
pip install scikit-learn pandas numpy matplotlib jupyter
```

3. Open the notebook:

```bash
jupyter notebook Digits_Handwriting_Model_Jupyter.ipynb
```

4. Run the cells from top to bottom. The dataset loads automatically, so no extra downloads are needed.

## What you'll see

As you run the notebook, you'll see the accuracy scores printed for each model and each cross-validation method. This lets you compare how the models perform and observe how the evaluation method affects the results.

## Notes

This is a learning project built to practice and demonstrate model comparison and cross-validation in scikit-learn. The digits dataset is small and clean, which makes it a good starting point for understanding these concepts before moving on to larger, messier datasets.


Happy coding everyone 🦊
   
