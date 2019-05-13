# finalproject
Final Project For Data To Models

### A guide to this code
1. `Preprocess.ipynb`: Data was preprocessed going from `presidential_general_polls.csv` to `full_data.csv`.
2. `Preproc_results.ipynb`: Puts unorganized election data into organized `results.csv` which includes clinton%, electoral votes, and poll closing time for each state.
2. `Impute.ipynb`: Used MICE 10 times to create 10 filled data matrices. Saved list to pkl file as `data_fill.pkl`. Subtract means to make gaussian easier and save for later in `means.pkl`
3. `Learn_PC.ipynb`: Used PCAlg to learn DAG for each MICE filled graph using BIC score to select best alpha each time. Analyzed results and saved DAG that takes only values that are in 5 or more learned DAGs in `DAG_PC.csv`
4. `Learn_MRF.ipynb`: Used Glasso to learn MRF for each MICE filled graph. Analyzed results and saved MRF that takes only values that are in 5 or more learned MRFs in `MRF.csv`. Save MRF using MLE for weights.
5. `MLE_Gaussian.ipynb` learns MLES for Gaussian models for PC DAGs. Saves to `MLE_PC.pkl`
6. `MCMC.ipynb`: Do conditional queries from DAG and MRF using both simple Metropolis Hastings algo and Goodman & Weare’s Affine Invariant Markov chain Monte Carlo (MCMC) Ensemble sampler. For DAG and MRF keep track of electoral votes and clinton percentage in each swing state after results come in for different time slots. Save to pickle files of the form `<MODEL>_<MCMC_TYPE>_<TIME>.pkl`
7. `Explore.ipynb`: I explore the results and make some tables and graphs.