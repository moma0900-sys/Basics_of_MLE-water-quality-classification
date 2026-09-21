# Basics of Machine Learning Modeling

This repository contains a sequence of short notebooks that introduce and refresh core Machine Learning workflows step by step. You will train models with scikit-learn, choose and interpret evaluation metrics for both classification and regression, scale features, define custom scorers, and tune hyperparameters. An optional exercise at the end ties the pieces together into one complete workflow.

## Learning Objectives

By the end of this repository, you should be able to:

- Explain the standard scikit-learn workflow of splitting data, fitting a model, predicting and evaluating.
- Choose suitable evaluation metrics for classification and regression problems.
- Interpret common classification metrics such as precision, recall, F1 score, ROC-AUC and precision-recall curves.
- Interpret common regression metrics such as MAE, MSE, RMSE, R² and MAPE.
- Apply `StandardScaler` correctly and explain when feature scaling matters.
- Build a custom scorer with `make_scorer` and tune hyperparameters using cross-validation, `RandomizedSearchCV`, `GridSearchCV`, and Optuna.

## Learning Path

Work through the files in order. Each one builds on the previous.

| File / Folder | Description |
|---|---|
| [**01 - Intro**](01-intro.md) | Introduction to basic Machine Learning concepts. |
| [**02 - ML Modeling with scikit-learn**](02-ml-model-sklearn.ipynb) | The basic scikit-learn estimator workflow: split, fit, predict, evaluate. |
| [**03 - Evaluation Metrics for Classification**](03-evaluation-metrics-for-classification.ipynb) | Common classification metrics and how to interpret them. |
| [**04 - Regression Metrics**](04-regression-metrics.ipynb) | Common regression metrics and what each one emphasizes. |
| [**05 - Customized Evaluation Metric**](05-customized-evaluation-metric.ipynb) | How to build a custom scorer with `make_scorer`. |
| [**06 - Feature Scaling**](06-feature-scaling.ipynb) | Why feature scaling matters for distance-based models. |
| [**07 - Hyperparameter Tuning**](07-hyperparameter-tuning.ipynb) | Cross-validation, `RandomizedSearchCV`, `GridSearchCV`, and Optuna. |
| [**08 - Exercise (Optional)**](08-OPTIONAL-exercise.md) | Guided exercise that combines the earlier concepts into one workflow. |
| [**08 - Exercise Solution (Optional)**](08-OPTIONAL-solution.ipynb) | One possible worked solution to the optional exercise. |

### Additional Folders and Files

| File / Folder | Description |
|---|---|
| [**data**](data/) | Datasets used across the notebooks and the optional exercise. |
| [**pyproject.toml**](pyproject.toml) | Project configuration and dependencies. |
| [**uv.lock**](uv.lock) | Dependency lock file. |

## Setup
> [!NOTE]
> Throughout these steps, text in angle brackets like `<repo-name>` is a
> **placeholder**. Replace it including the `< >` brackets with your own
> value. For example, `cd <repo-name>` becomes `cd mle-basics-of-ml`.

### 1. Create the Repository from the Template

Click **Use this template** on GitHub.

When creating the repository:

- Set yourself as the **Owner**
- Choose a repository name
- Disable **Include all branches**
- Click **Create repository**

> [!IMPORTANT]
> If you are working in pairs or groups, only **one person** should complete this step.

---

### 2. Add Collaborators (Pairs/Groups Only)

If working with teammates:

1. Open the repository on GitHub
2. Go to **Settings → Collaborators**
3. Add your teammates as collaborators
4. Share the repository link with your team

Teammates should accept the invitation before continuing.

---

### 3. Clone the Repository

Copy the SSH URL from the **Code** button on GitHub, then run:

```bash
git clone <copied-ssh-url>
```

The copied SSH URL will look like `git@github.com:<your-username>/<repo-name>.git`.

---

### 4. Move into the Project Folder and Install Dependencies

This installs all dependencies and creates a virtual environment in `.venv/`.

```bash
cd <repo-name>
uv sync
```

---

### 5. Open the Notebooks

> [!NOTE]
> Make sure you open VS Code from the project root so it automatically detects the environment created by uv sync.

Launch VS Code in the project root folder:

```bash
code .
```

Then open a notebook and select the Python environment created by `uv sync` as the kernel.

## References & Further Reading

- [Metrics and Scoring](https://scikit-learn.org/stable/modules/model_evaluation.html): The scikit-learn reference for every classification and regression metric used here, including `make_scorer`.
- [Cross-validation](https://scikit-learn.org/stable/modules/cross_validation.html): How `cross_validate` and the various splitting strategies work.
- [Hyperparameter Tuning](https://scikit-learn.org/stable/modules/grid_search.html): The official guide to `GridSearchCV` and `RandomizedSearchCV`.
- [Optuna Docs](https://optuna.readthedocs.io/en/stable/): Getting started with the optimization framework used in notebook 07.
