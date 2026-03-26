AIML420 Assignment 1 - Part 2: Exploring Classification Algorithms
====================================================================

DEPENDENCIES
------------
Python 3.11+
Required packages: numpy, pandas, matplotlib, scikit-learn, jupyter

SETUP
-----
    python3 -m venv venv
    source venv/bin/activate
    pip install -r ../requirements.txt

HOW TO RUN
----------
Option 1 - Interactive (Jupyter Notebook):
    jupyter notebook Part_2_Classification_Algorithms.ipynb

Option 2 - Command line (non-interactive):
    jupyter nbconvert --to notebook --execute Part_2_Classification_Algorithms.ipynb

Run all cells sequentially. No manual configuration needed.

FILES
-----
Part_2_Classification_Algorithms.ipynb  - Main notebook
breast-cancer.csv                       - Input dataset (Wisconsin Breast Cancer)

KNOWN BUGS
----------
None. The program runs without errors.

SAMPLE OUTPUT
-------------

--- Missing Data Handling ---

========================================
Mean Imputation:
Accuracy: 0.9181
Precision: 0.8611
Recall: 0.9394
F1 Score: 0.8986

----------------------------------------

Median Imputation:
Accuracy: 0.9181
Precision: 0.8611
Recall: 0.9394
F1 Score: 0.8986

========================================

--- Normalisation Comparison ---

Model Normalization  Accuracy  Precision   Recall       F1
  KNN          None  0.918129   0.933333 0.848485 0.888889
   DT          None  0.918129   0.861111 0.939394 0.898551
  KNN        MinMax  0.964912   0.968750 0.939394 0.953846
   DT        MinMax  0.918129   0.861111 0.939394 0.898551
  KNN      Standard  0.970760   0.984127 0.939394 0.961240
   DT      Standard  0.918129   0.861111 0.939394 0.898551

--- Hyperparameter Tuning ---

KNN with k=3: Accuracy=0.9708, Precision=0.9692, Recall=0.9545, F1=0.9618
KNN with k=9: Accuracy=0.9708, Precision=0.9841, Recall=0.9394, F1=0.9612
KNN with k=15: Accuracy=0.9825, Precision=1.0000, Recall=0.9545, F1=0.9767
KNN with k=21: Accuracy=0.9591, Precision=1.0000, Recall=0.8939, F1=0.9440

Decision Tree with max_depth=2: Accuracy=0.8947, Precision=0.8429, Recall=0.8939, F1=0.8676
Decision Tree with max_depth=8: Accuracy=0.9181, Precision=0.8611, Recall=0.9394, F1=0.8986
Decision Tree with max_depth=14: Accuracy=0.9181, Precision=0.8611, Recall=0.9394, F1=0.8986

AdaBoost with n_estimators=10: Accuracy=0.9474, Precision=0.9014, Recall=0.9697, F1=0.9343
AdaBoost with n_estimators=20: Accuracy=0.9532, Precision=0.9143, Recall=0.9697, F1=0.9412
AdaBoost with n_estimators=30: Accuracy=0.9532, Precision=0.9143, Recall=0.9697, F1=0.9412

Random Forest with n_estimators=10: Accuracy=0.9357, Precision=0.9104, Recall=0.9242, F1=0.9173
Random Forest with n_estimators=30: Accuracy=0.9415, Precision=0.9375, Recall=0.9091, F1=0.9231
Random Forest with n_estimators=50: Accuracy=0.9532, Precision=0.9677, Recall=0.9091, F1=0.9375
Random Forest with n_estimators=60: Accuracy=0.9591, Precision=0.9683, Recall=0.9242, F1=0.9457

--- Feature Selection (Pearson Correlation, threshold > 0.6) ---

Decision Tree with selected features: Accuracy=0.9064, Precision=0.8472, Recall=0.9242, F1=0.8841

Features  Accuracy  Precision   Recall       F1
     All  0.918129   0.861111 0.939394 0.898551
Selected  0.906433   0.847222 0.924242 0.884058

--- PCA (95% variance retained, 10 components) ---

   Depth  PCA  Accuracy  Precision    Recall        F1
       2   No  0.894737   0.842857  0.893939  0.867647
       2  Yes  0.888889   0.850746  0.863636  0.857143
       8   No  0.918129   0.861111  0.939394  0.898551
       8  Yes  0.935673   0.936508  0.893939  0.914729
