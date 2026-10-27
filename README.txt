CS7CS4 Machine Learning - Week 2 Assignment
Hera Khan | Student ID: 22312194

HOW TO RUN
1. Unzip this folder.
2. Install the packages:
       pip install -r requirements.txt
3. Run the script from inside this folder:
       python assignment1_ml_final.py
   Plot windows open one at a time; close each one to continue.

FILES
- assignment1_ml_final.py   Main script (parts a, b and c of the assignment).
- week2.csv                 Dataset used by the script. This is my downloaded
                            data with the "# id:14-14-14" header line removed
                            so the script can read it directly.
- requirements.txt          Python packages needed (numpy, pandas, matplotlib,
                            scikit-learn).
- reference/                For reference only, not needed to run the script:
    week2_original.csv          The unmodified download (includes the header line).
    assignment1_ml_final.ipynb  Notebook version of the same code.

NOTE
week2.csv must stay in the same folder as the .py file.

What I did

Visualised the classes; the -1 points form a dome, so a straight line cannot separate them.
Trained logistic regression and read the parameters (the second feature dominates, about 37x the first) and derived the decision boundary from them.
Trained LinearSVC for C = 0.001, 1, 100 and compared parameters and boundaries with logistic regression.
Added squared features (x1², x2²) to give a curved boundary.
Evaluated with confusion matrices, precision, recall, F1 and a majority-class baseline.

Results

Logistic regression: 85.0% test accuracy (precision 0.88, recall 0.90).
LinearSVC: also 85.0% for every C. The weights grow with C (θ2: 0.37 → 1.07 → 1.08) but the boundary barely moves, so a linear model hits a structural limit on this data.
With squared features: 96.25% test accuracy.
Majority-class baseline: 66.5%.