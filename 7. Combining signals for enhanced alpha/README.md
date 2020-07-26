# Combining signals for enhanced alpha

This project contains

  1. Implementing random forest to predict 5 days later returns
  2. Comparing the performance of three ways of solving _the overlapping labels
  
    1) not using overlapping samples
    2) Using Bagging-classifier with the ratio of max_samples
    3) Building an ensemble of non-overlapping trees
    
  3. Evaluating each model with Sharpe ratio (mean/stdv.) and factor rank autocorrelation.
    
   
 
 # Requirements
 
  * alphalens==0.3.2
  * graphviz==0.10.1
  * numpy==1.13.3
  * pandas==0.18.1
  * python-dateutil==2.6.1
  * pytz==2017.3
  * scipy==1.0.0
  * scikit-learn==0.19.1
  * six==1.11.0
  * tables==3.3.0
  * tqdm==4.19.5
  * zipline===1.2.0

  
 # How to run
 
Please execute all the command lines in Combining_signals_for_enhanced_alpha.ipynb, where results are.

# Experiment results

The model performing the best is 3) building an ensemble of non-overlapping trees, and this leads to positive alpha with test data.

