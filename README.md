# FINAM_HOTEL_REVIEWS

## Project Overview
This project focuses on **text classification and topic modeling** for text hotels reviews data. The goal is to preprocess, analyze, and cluster financial reviews using Natural Language Processing (NLP) techniques, such as **TF-IDF, embeddings, clusters and LDA**.

## Directory Structure
```
FINAM_TOPIC_MODELLING/
│── .venv/                   # Virtual environment
│── data/
│   ├── interim/             # Intermediate processed data
│   ├── processed/           # Final processed data
│   ├── raw/                 # Raw datasets
│── models/                  # Trained models
│── notebooks/               # Jupyter Notebooks for analysis
│── reports/                 # Reports and visualizations
│── .gitignore               # Git ignore file
│── pyproject.toml           # PDM project configuration
│── pdm.lock                 # Pinned dependencies
│── requirements.txt         # Dependencies for the project
│── README.md                # Project documentation
│── solution.md              # Project findings and insights
```

## Installation
This project uses **PDM** for dependency management. To set up the environment:

```sh
pdm install
```

If you prefer using `pip`, install dependencies from:

```sh
pip install -r requirements.txt
```

## Data Sources
- **Raw Data**: Located in `data/raw/`
- **Processed Data**: Cleaned and transformed data in `data/processed/`
- **Intermediate Data**: Stored in `data/interim/` during preprocessing

## Notebooks
The `notebooks/` directory contains step-by-step analyses:
1. `00_first_small_eda.ipynb` - Initial exploratory data analysis
2. `01_cleaning_lemmatization.ipynb` - Text preprocessing pipeline
3. `02_process_embedding.ipynb` - Generating embeddings
4. `03_clustering_analyses.ipynb` - Clustering financial reviews
5. `04_topic_modelling_with_lda.ipynb` - LDA topic modeling

## Model Training
Trained models are stored in `models/`. The workflow includes:
1. Text preprocessing (tokenization, stopword removal, lemmatization)
2. Feature extraction (TF-IDF, Word2Vec, BERT embeddings)
3. Clustering techniques (K-Means, HDBSCAN)
4. Topic modeling using **LDA (Latent Dirichlet Allocation)**

## Running the Project
To execute preprocessing and modeling:
```sh
pdm run python scripts/preprocess.py
pdm run python scripts/train_model.py
```

## Results & Reports
- `reports/html/` contains interactive visualizations
- `reports/ipynb/` contains Jupyter-based reports

## Dependencies
- Python 3.x
- pandas, numpy, scikit-learn
- nltk, spacy, gensim
- pyLDAvis, seaborn, matplotlib
- transformers, torch (for embeddings)

## Contribution
1. Clone the repository:
   ```sh
   git clone https://github.com/your-repo/FINAM_TOPIC_MODELLING.git
   ```
2. Create a new branch:
   ```sh
   git checkout -b feature-branch
   ```
3. Commit changes and push:
   ```sh
   git commit -m "Added new feature"
   git push origin feature-branch
   ```
4. Submit a pull request.

## License
MIT License

---


