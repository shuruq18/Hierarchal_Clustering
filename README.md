
# Hierarchical Clustering on Breast Cancer Data

An unsupervised machine learning project applying Agglomerative Hierarchical Clustering to the UCI Breast Cancer dataset, with dendrogram and scatter plot visualizations.

---

## Overview

This project demonstrates how to apply **Agglomerative Clustering** — a bottom-up hierarchical clustering algorithm — to real-world medical data. The breast cancer dataset is used to explore natural groupings within the feature space, visualized through dendrograms and 2D scatter plots for both training and test sets.

---

## How It Works

### Algorithm: Agglomerative Clustering

Agglomerative clustering starts by treating each data point as its own cluster, then iteratively merges the closest pairs of clusters until the desired number (`n_clusters`) is reached.

**Configuration used:**

| Parameter  | Value       | Options                                      |
|------------|-------------|----------------------------------------------|
| `n_clusters` | 5         | Any positive integer                         |
| `metric`   | `euclidean` | `l1`, `l2`, `manhattan`, `cosine`, `precomputed` |
| `linkage`  | `ward`      | `complete`, `average`, `single`              |

### Visualizations

Two types of plots are generated for both the training and test sets:

- **Dendrograms** — show the hierarchical merging of the first 30 samples, illustrating distances between clusters at each merge step
- **Scatter plots** — display the 5 clusters in 2D space (using the first two features), each cluster color-coded for easy interpretation

---

## Dataset

- **Source:** `sklearn.datasets.load_breast_cancer()` — built into scikit-learn, no download needed
- **Samples:** 569 total (383 train / 186 test with a 67/33 split)
- **Features:** 30 numeric features (e.g., mean radius, texture, perimeter, area, smoothness)
- **Original Labels:** Malignant / Benign (not used during clustering — this is unsupervised)

---

## Project Structure

```
├── Hierarchal_Clustering.ipynb   # Main notebook
```

---

## Requirements

```
scikit-learn
scipy
matplotlib
numpy
```

Install dependencies with:

```bash
pip install scikit-learn scipy matplotlib numpy
```

---

## Usage

1. Clone the repository and navigate to the project folder.
2. Open and run the notebook:

```bash
jupyter notebook Hierarchal_Clustering.ipynb
```

No external data files are needed — the breast cancer dataset loads directly from scikit-learn.

---

## Key Concepts

- **Agglomerative Clustering** — bottom-up hierarchical clustering that merges nearest clusters iteratively
- **Ward Linkage** — minimizes the total within-cluster variance at each merge step; tends to produce compact, evenly-sized clusters
- **Dendrogram** — a tree diagram that shows the sequence and distances of cluster merges, useful for choosing the optimal number of clusters
- **Unsupervised Learning** — no labels are used during training; the algorithm finds structure in the data on its own

---

## References

- [scikit-learn: AgglomerativeClustering](https://scikit-learn.org/stable/modules/generated/sklearn.cluster.AgglomerativeClustering.html)
- [scipy: Hierarchical Clustering](https://docs.scipy.org/doc/scipy/reference/cluster.hierarchy.html)
- [UCI Breast Cancer Dataset](https://scikit-learn.org/stable/datasets/toy_dataset.html#breast-cancer-dataset)
