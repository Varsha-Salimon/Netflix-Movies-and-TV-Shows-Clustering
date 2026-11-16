# Netflix Movies and TV Shows Clustering

An unsupervised machine-learning capstone exploring similarities among Netflix catalogue titles using descriptions and catalogue metadata.

## Project objective

Explore thematic groupings of Movies and TV Shows using TF-IDF text features and compare K-Means, MiniBatch K-Means, and Agglomerative Clustering. The output is intended for exploratory catalogue analysis; it is not a Netflix classification system or a personalized recommendation engine.

## Dataset

The notebook uses the Netflix Movies and TV Shows CSV (7,787 rows and 12 columns in the supplied snapshot). The CSV is downloaded in the notebook from a Google Drive file ID. Ensure that the file is shared as **Anyone with the link — Viewer** before running the notebook.

## Workflow

1. Load and inspect the catalogue data.
2. Clean fields and parse date-added information.
3. Perform exploratory analysis and hypothesis tests.
4. Construct text features from description, genre/category, content type, and rating.
5. Apply text preprocessing and TF-IDF vectorization.
6. Compare K-Means, MiniBatch K-Means, and sample-based Agglomerative Clustering.
7. Interpret clusters using top TF-IDF terms and representative titles.
8. Save and reload the selected exploratory K-Means baseline.

## Models and limitations

K-Means is retained as the practical baseline for the full sparse TF-IDF catalogue. The saved five-cluster silhouette score is approximately 0.0200, indicating weak separation. MiniBatch K-Means scored approximately 0.0183 in the saved comparison. Agglomerative Clustering is evaluated on a 1,500-title sample after TruncatedSVD; its scores are not directly comparable with the full-space K-Means results.

The dataset does not include viewing histories, engagement, revenue, or licensing information. Cluster assignments should not be interpreted as viewer preferences, commercial success, or personalized recommendations.

## Run the notebook

1. Open the notebook in Google Colab.
2. Confirm the Google Drive CSV is shared with link-viewer access.
3. Select **Runtime → Run all**.
4. Review the outputs and confirm that the model artifact is saved successfully.

Required libraries are imported/installed in the notebook, including pandas, NumPy, matplotlib, seaborn, scikit-learn, joblib, gdown, and NLTK.

## Files

- `Netflix_Movies_TV_Shows_Clustering.ipynb` — colab notebook.

## Author

Varsha S
