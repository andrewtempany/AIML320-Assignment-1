AIML420 Assignment 1 - Part 1: Decision Tree from Scratch
==========================================================

DEPENDENCIES
------------
Python 3.11+
Required packages: numpy, matplotlib, jupyter

SETUP
-----
    python3 -m venv venv
    source venv/bin/activate
    pip install -r ../requirements.txt

HOW TO RUN
----------
Option 1 - Interactive (Jupyter Notebook):
    jupyter notebook Part_1_Decision_Tree.ipynb

Option 2 - Command line (non-interactive):
    jupyter nbconvert --to notebook --execute Part_1_Decision_Tree.ipynb

The notebook loads one dataset at a time. To switch datasets, change the
csv_file variable in the data loading cell:

    csv_file = '../data_part1/rtg_A.csv'
    # csv_file = '../data_part1/rtg_B.csv'
    # csv_file = '../data_part1/rtg_C.csv'

Also update the output_file variable in the output cell to match:

    output_file = "output_tree_A.txt"

FILES
-----
Part_1_Decision_Tree.ipynb  - Main notebook (Decision Tree implemented from scratch)
output_tree_A.txt           - Generated tree output for rtg_A dataset
output_tree_B.txt           - Generated tree output for rtg_B dataset
output_tree_C.txt           - Generated tree output for rtg_C dataset
../data_part1/              - Input datasets (rtg_A.csv, rtg_B.csv, rtg_C.csv)

KNOWN BUGS
----------
None. The program runs without errors.

SAMPLE OUTPUT (rtg_A dataset)
-----------------------------
Features: ['att0', 'att1', 'att2', 'att3']
Overall Accuracy: 100.0%  (100/100 correct)

70/30 Test Accuracy: 100.0%  (30/30)

att0         0.116673        0.0             ✓ YES
att2         0.098343        0.0             ✓ YES
att1         0.090168        0.0             ✓ YES
att3         0.000000        None            ✗ NO
======================================================================

Features actually used in final tree: ['att0', 'att1', 'att2']
Features NOT used: ['att3']

Tree written to: output_tree_A.txt
