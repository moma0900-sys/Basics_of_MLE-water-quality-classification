# Optional Exercise: Build, Evaluate, and Tune a Model

This exercise is your chance to combine the ideas from the previous notebooks into one small machine learning workflow.

Your task is to choose **one** of the provided datasets and build a complete solution from start to finish:

- [`data/movies.csv`](data/movies.csv)
- [`data/water-quality.csv`](data/water-quality.csv)
- [`data/wine-quality.csv`](data/wine-quality.csv) (harder)

> [!NOTE]
> `wine-quality.csv` is the stretch option. `quality` is an ordinal score from 3 to 9, so you can treat it either as multi-class classification with 7 classes or as regression whose predictions you round back to whole scores. Either way, the classes are severely imbalanced: 2198 wines score 6, but only 5 score 9.

## Your Goal

Train a model, evaluate it with a sensible metric, and improve it with hyperparameter tuning.

## Suggested Workflow

1. Pick a dataset and identify the target column.
2. Decide whether your problem is a classification or regression task.
3. Choose a reasonable baseline model.
4. Split the data into training and test sets.
5. Scale the features if your model depends on feature magnitudes.
6. Train the model and evaluate it with an appropriate metric.
7. Tune one or more hyperparameters with a search method such as `RandomizedSearchCV`, `GridSearchCV`, or Optuna.
8. Compare the tuned model against your baseline and explain what changed.

## What to Keep in Mind

- If you use a distance-based or regularized model, scaling is usually important.
- Choose a metric that matches the problem.
- For imbalanced classification, accuracy alone is often not enough.
- Use cross-validation during tuning so that your result is more reliable than a single train-test split.

## Deliverables

By the end of the exercise, your notebook or script should show:

- the dataset you chose,
- the model you trained,
- the evaluation metric you selected and why,
- the baseline result,
- the tuned result,
- a short conclusion about whether tuning helped.

## Hints

- `water-quality.csv` is a classification problem with target column `is_safe`.
- `movies.csv` is a regression problem with target column `Collection`.
- Load `wine-quality.csv` with `pd.read_csv("data/wine-quality.csv", sep=";")`. Its target column is `quality`; choose multi-class classification or regression as described above.
- For wine-quality classification, use a multi-class metric such as macro F1 (`scoring="f1_macro"`), not the binary F1 scorer used in the water-quality examples. Choose the number of cross-validation folds based on the smallest class in your training split.
- A `Pipeline` can help combine scaling and modeling cleanly.
- `RandomizedSearchCV` is often a good first tuning method because it is faster than checking every combination in a grid.

## Optional Solution

If you want a worked example after trying the exercise yourself, open [`08-OPTIONAL-solution.ipynb`](08-OPTIONAL-solution.ipynb).
