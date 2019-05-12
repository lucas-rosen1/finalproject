# finalproject
Final Project For Data To Models

### A guide to this code
1. `Preprocess.ipynb`: Data was preprocessed going from `presidential_general_polls.csv` to `full_data.csv`
2. `Impute.ipynb`: Used MICE 10 times to create 10 filled data matrices. Saved list to pkl file as `data_fill.pkl`
3. `Learn_MRF.ipynb`: Used graphical LASSO to learn MRF using CV for lambda parameter for each MICE filled graph and analyzed results. Saved MRF that takes only values that are in 5 or more learned MRFs in `MRF.npy` 
4. `Learn_DAG.ipynb`: Used PCAlg to learn DAG for each MICE filled graph using BIC score to select best alpha each time. Analyzed results and saved DAG that takes only values that are in 5 or more learned DAGs in `DAG.npy`