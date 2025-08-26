Class Activity: Kaggle + GitHub (Fork & PR)

Welcome to our class activity. We’ll combine Kaggle exploration with GitHub collaboration to collect observations from the Iris dataset.

What You’ll Do

Open the Iris dataset in a Kaggle Notebook.

Explore the dataset for a few minutes and write one simple observation about it. Examples:

“The dataset has 150 rows and 5 columns.”

“Species column has 3 unique values: setosa, versicolor, virginica.”

“Each species has 50 samples.”

“No missing values in any column.”

Fork this GitHub repo into your account.

Open observations.md in your fork.

Add your Name + Observation at the bottom. Format exactly like this:

- YourName: Your one-line observation


Commit your changes.

Open a Pull Request to this main repo so your contribution can be merged.

Notebook Code Snippets

You can copy-paste these into your Kaggle notebook to explore the Iris dataset.

# 1. Load the dataset
import seaborn as sns
df = sns.load_dataset("iris")

# 2. First few rows
print(df.head())

# 3. Dataset shape (rows, columns)
print(df.shape)

# 4. Column info
print(df.info())

# 5. Summary statistics
print(df.describe())

# 6. Unique species and counts
print(df['species'].unique())
print(df['species'].value_counts())

# 7. Missing values check
print(df.isnull().sum())

# 8. Average measurements by species
print(df.groupby('species').mean())

About Pull Requests

A Pull Request (PR) is how you suggest changes to someone else’s repository.

Steps in short:

Fork the repo.

Make changes in your fork.

Open a Pull Request to the main repo.

The owner reviews and merges it.

Think of it like copying a document, making edits, and asking the owner: “Do you want to include my changes?”

Tips

Make sure your commit message is clear. Example: “Added my observation — John”.

Add your observation at the bottom to avoid conflicts.



code:



Optionally, upload your Kaggle notebook (.ipynb) and include a link in your PR.

Goal

By the end of the session, the repo will contain everyone’s observations from the Iris dataset. This activity shows how data exploration on Kaggle and collaboration on GitHub work together.


code
# 1. Load the dataset
import seaborn as sns
df = sns.load_dataset("iris")

# 2. First few rows
print(df.head())

# 3. Dataset shape (rows, columns)
print(df.shape)

# 4. Column info
print(df.info())

# 5. Summary statistics
print(df.describe())

# 6. Unique species and counts
print(df['species'].unique())
print(df['species'].value_counts())

# 7. Missing values check
print(df.isnull().sum())

# 8. Average measurements by species
print(df.groupby('species').mean())

alternate code (if first one doesnt work)
# offline-safe way to load iris dataset
from sklearn.datasets import load_iris
import pandas as pd

# load iris dataset
data = load_iris(as_frame=True)
df = data.frame

# rename target column to species
df.rename(columns={'target': 'species'}, inplace=True)
df['species'] = df['species'].map({0:'setosa', 1:'versicolor', 2:'virginica'})

# preview the dataframe
print(df.head())

# examples of exploration
print(df.shape)
print(df.info())
print(df.describe())
print(df['species'].value_counts())
print(df.isnull().sum())
print(df.groupby('species').mean())



