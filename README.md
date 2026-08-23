# 🫀 Clinical Feature Selection & Interpretability Analysis for Heart Disease Prediction

This project evaluates multiple feature selection frameworks (Filter, Wrapper, and Embedded methods) against Dimensionality Reduction (PCA) on the Heart Disease Dataset, focusing on classification accuracy and clinical interpretability.

---

## 🛠️ Methodologies Implemented

- **Correlation-based Filtering:** Evaluated multicollinearity across clinical attributes.
- **Univariate Selection:** Ranked features using Mutual Information metrics.
- **Recursive Feature Elimination (RFE & RFECV):** Performed iterative feature pruning combined with K-Fold Cross-Validation to identify the optimal subset size.
- **Embedded Regularization (Lasso L1):** Leveraged $L_1$ penalty coefficient sparsity for feature ranking.
- **PCA vs. Feature Selection Comparison:** Analyzed variance preservation versus feature interpretability in medical domain contexts.

---

## 📊 Summary of Results

- **Filter Methods:** Low inter-feature correlation ($<0.58$) indicated minimal direct redundancy, keeping initial features intact.
- **RFE vs. Mutual Information:** RFE achieved **80% accuracy** with 5 features (`sex`, `cp`, `exang`, `oldpeak`, `thal`), outperforming Mutual Information (73%) by capturing feature interactions.
- **Optimal Subset (RFECV):** Identified **11 optimal features**, improving validation accuracy from 71% to **~86%**.
- **Lasso & PCA:** Lasso retained 12 clinically significant features (zeroing `fbs`). PCA required 12 components to cover 95% of variance, confirming that feature selection preserves raw clinical meaning far better than component combination.
