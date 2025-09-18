# Matrix Factorization Recommender System 
A study of collaborative filtering with matrix factorization using the Alternating Least Squares (ALS) algorithm, applied to the **MovieLens 100K** dataset. Includes enhancements such as early stopping, diversity-aware recommendation, and latent factor visualization.  

---

## 📂 Repository Structure
```bash
├── movielens-als-recommender.ipynb      # Jupyter Notebook with code & experiments
├── requirements.txt         # Python dependencies
└── README.md                # Project documentation
```

## 📖 Contents
## 1. Matrix Factorization with ALS
- Implementation of ALS optimization alternating between user and item factor updates.
- Incorporation of user, item, and global bias terms.
- Regularization and numerical stability handling.

## 2. Model Training & Evaluation
- Dataset split into 60% training, 20% validation, 20% test.
- Experiments with latent factors (k ∈ {5, 10, 20, 50}).
- Early stopping mechanism based on validation RMSE.
- Performance metrics: RMSE on training, validation, and test sets.

## 3. Recommendation Generation
- Top-N recommendation based on predicted ratings.
- Diversity-aware mode: includes underrepresented genres.
- Genre alignment analysis to evaluate recommendation quality.

## 4. Visualization of Latent Factors
- PCA and t-SNE projections of item embeddings.
- Exploration of clustering patterns by genre.

## 5. Challenges & Solutions
- Matrix sparsity handled with dictionary-based representation.
- Cold-start fallback with global mean rating.
- Overfitting mitigated with early stopping and validation monitoring.

---

## ⚙️ Requirements

To run the notebook, install the following dependencies:
```
pip install -r requirements.txt
```

(Alternatively, install manually:)
```
pip install numpy pandas matplotlib scikit-learn
```
---
## 🚀 How to Run

Clone this repository:
```
git clone https://github.com/tamerbegum/matrix-factorization-recommender.git
cd matrix-factorization-recommender
```

Open the Jupyter Notebook:
```
jupyter notebook movielens-als-recommender.ipynb
```

Run the cells step by step to reproduce the results.

---

## 📊 Results

Best configuration: k = 50 latent factors.

Training RMSE: 0.5636

Validation RMSE: 0.9212

Test RMSE: 0.9277

Example recommendations showed 80% genre alignment with users’ preferences.

---

## ✨ Acknowledgments
- This project was developed during my MSc Digital Business Engineering program.
- Dataset: MovieLens 100K
- Code and explanations were developed independently, guided by course materials and supplemented with insights from ChatGPT (reviewed and adapted to ensure originality).
