# Decision Trees

A hands-on introduction to the decision tree algorithm in Python. You build trees for both classification and regression with scikit-learn, visualise how they split the data, tune them to control overfitting, apply a classifier to a real public-health dataset, and finish by recapping the core ideas alongside a tree built from scratch.

## Learning Objectives

By the end of this repository, you should be able to:

- Build decision tree classifiers and regressors with scikit-learn.
- Visualise a fitted tree and its decision boundaries.
- Tune hyperparameters such as `max_depth` to manage overfitting.
- Compare splitting criteria (Gini impurity and entropy) and trace how splits are chosen.
- Evaluate a model on imbalanced data using a baseline, a metric, and error analysis.
- Rank feature importances to explain a tree's predictions.

## Learning Path

Work through the notebooks in order. Pairing up and explaining each step to a partner is a good way to test your understanding.

| File / Folder                                                            | Description                                                                                                                  |
| ------------------------------------------------------------------------ | ---------------------------------------------------------------------------------------------------------------------------- |
| [**1 - Visualisation**](1_decision_trees_visualization.ipynb)            | Build classification and regression trees on small datasets, then plot the trees and their decision boundaries.              |
| [**2 - Classification**](2_decision_trees_classification.ipynb)          | Apply a classifier to a real, imbalanced health survey: metric choice, baseline model, error analysis, and feature importance. |
| [**3 - Recap**](3_decision_trees_recap.ipynb)                            | Recap the key concepts and step through a decision tree built from scratch in pure Python.                                   |

### Additional Folders and Files

| File / Folder                                                            | Description                                                  |
| ------------------------------------------------------------------------ | ----------------------------------------------------------- |
| [**Helper and Plotting Functions**](helper_and_plotting_functions.py)    | Shared functions for evaluating models and plotting results. |
| [**Solutions**](solutions/)                                              | Reference solutions.                                        |
| [**Assets**](assets/)                                                    | Diagram files: the tree SVG and an Excalidraw recap board.  |
| [**Codebook Report**](llcp_2022_codebook_report.pdf)                     | Column descriptions for the BRFSS survey dataset.           |
| [**data.zip**](data.zip)                                                 | The dataset, bundled as a zip (unzip it during setup).      |
| [**pyproject.toml**](pyproject.toml)                                     | Project configuration and dependencies.                     |
| [**uv.lock**](uv.lock)                                                   | Dependency lock file.                                       |

## Setup

> [!NOTE]
> Throughout these steps, text in angle brackets like `<repo-name>` is a **placeholder**. Replace it including the `< >` brackets with your own value. For example, `cd <repo-name>` becomes `cd ds-decision-tree`.

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

This installs all dependencies and creates a virtual environment in (`.venv/`).

```bash
cd <repo-name>
uv sync
```

---

### 5. Unzip the Data

The dataset is bundled in `data.zip`. Extract it into a `data/` folder before running the notebooks. This command uses the environment from `uv sync`:

```bash
uv run python -c "import zipfile; zipfile.ZipFile('data.zip').extractall()"
```

---

### 6. Open the Notebooks

> [!NOTE]
> Make sure you open VS Code from the project root so it automatically detects the environment created by `uv sync`.

Launch VS Code in the project root folder:

```bash
code .
```

Then open a notebook and select the Python environment created by `uv sync` as the kernel.

## References & Further Reading

- [**Scikit-learn: Decision Trees**](https://scikit-learn.org/stable/modules/tree.html): User guide covering classifiers, regressors, splitting criteria, and pruning.
- [**Scikit-learn: DecisionTreeClassifier**](https://scikit-learn.org/stable/modules/generated/sklearn.tree.DecisionTreeClassifier.html): The API reference for the classifier used here.
- [**How to Calculate Feature Importance With Python**](https://machinelearningmastery.com/calculate-feature-importance-with-python/): Practical walkthrough of feature-importance methods, including tree-based importance.
- [**Behavioral Risk Factor Surveillance System 2022 (Kaggle)**](https://www.kaggle.com/datasets/ariaxiong/behavioral-risk-factor-surveillance-system-2022/data): The full public-health dataset the classification notebook samples from.
