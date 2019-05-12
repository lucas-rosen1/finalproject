# finalproject
Final Project For Data To Models

### A guide to this code
1. `Preprocess.ipynb`: Data was preprocessed going from `presidential_general_polls.csv` to `full_data.csv`
2. `Impute.ipynb`: Used MICE 10 times to create 10 filled data matrices. Saved list to pkl file as `data_fill.pkl`
3. `Learn_DAG.ipynb`: Used PCAlg to learn DAG for each MICE filled graph using BIC score to select best alpha each time. Analyzed results and saved DAG that takes only values that are in 5 or more learned DAGs in `DAG_PC.csv`
4. `Learn_GES.ipynb`: Used GES to learn DAG for each MICE filled graph. Analyzed results and saved DAG that takes only values that are in 5 or more learned DAGs in `DAG_PC.csv`