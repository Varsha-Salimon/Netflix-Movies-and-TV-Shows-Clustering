# Netflix Movies and TV Shows Clustering

An individual AlmaBetter capstone project using unsupervised machine learning to explore similarities among Netflix catalogue titles through synopsis text and catalogue metadata.

## Project objective

Explore thematic groupings of Movies and TV Shows using TF-IDF text features and compare K-Means, MiniBatch K-Means, and Agglomerative Clustering. This is an exploratory catalogue-analysis project, not an official Netflix classification system or a personalized recommendation engine.

## Dataset

The notebook uses the Netflix Movies and TV Shows CSV (7,787 rows and 12 columns in the supplied dataset snapshot). The CSV is downloaded in the notebook from a Google Drive file ID. For the download to work in a fresh Colab runtime, the CSV must be shared as **Anyone with the link — Viewer**.

## Workflow

1. Load and inspect the catalogue data.
2. Clean fields and parse date-added information.
3. Perform exploratory data analysis and hypothesis testing.
4. Construct text features from description, genre/category, content type, and rating.
5. Apply text preprocessing and TF-IDF vectorization.
6. Compare K-Means, MiniBatch K-Means, and sample-based Agglomerative Clustering.
7. Interpret clusters using top TF-IDF terms and representative titles.
8. Save and reload the selected exploratory K-Means baseline.

## Models and limitations

K-Means is used as the practical baseline for the full sparse TF-IDF catalogue. The notebook's recorded five-cluster silhouette score is approximately 0.0200, indicating weak separation. MiniBatch K-Means scored approximately 0.0183 in the recorded comparison. Agglomerative Clustering is evaluated on a 1,500-title sample after TruncatedSVD, so its scores are not directly comparable with the full-space K-Means results.

The dataset does not include viewing histories, engagement, revenue, or licensing information. Cluster assignments should not be interpreted as viewer preferences, commercial success, or personalized recommendations. Treat all reported metrics as the outputs of the notebook run and rerun the notebook to reproduce them.

## Run the notebook

1. Open [the notebook](Netflix_Movies_TV_Shows_Clustering.ipynb) in GitHub, or download it and upload it to [Google Colab](https://colab.research.google.com/).
2. Confirm that the Google Drive CSV is shared with link-viewer access.
3. In Colab, select **Runtime → Run all**.
4. Review the outputs and confirm that the model artifact is saved successfully.

The notebook installs/imports its required Python libraries, including pandas, NumPy, matplotlib, seaborn, scikit-learn, joblib, gdown, and NLTK.

## Repository contents

- `Netflix_Movies_TV_Shows_Clustering.ipynb` — project notebook.

The presentation script is intentionally not included in this repository.

## Author

Varsha S — Individual capstone project.
