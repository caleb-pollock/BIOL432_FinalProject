# BIOL432_FinalProject
Group repository for the final BIOL 432 group assignment for Green Thumbs
Team Name: Green Thumbs
Team Members: Edward Chen, Kerri Lynch, Igor Neder Serafini, Caleb Pollock, Rishona Vemulapalli
Dataset Website: https://zenodo.org/record/5008930
Dataset: https://zenodo.org/record/5008930/files/Soper_Gorden_Adler_AJB_2018_Flower_Insect_Interactions_Processed_Data.csv?download=1

To obtain the data, please download the dataset using the above link. The paper contains multiple dataset which we will not be investigating.

We have 3 questions to address:

Q1. Is it possible to predict the reproductive success of selfing and pollinated plants based on its flower-insect interactions? 

The analysis involves logistic regression on the number of flower-insect interactions vs seed mass. Furthermore, a NMDS is constructed individually for each group (CH or CL) to investigate the similarities and differences between the insects and flowers interactions. The code for this analysis is located in Q1.Rmd.

Q2. Can we determine which variables are important for separating the selfing and pollination mating types?

The preprocessing for the dataset is located in Q2_preprocess.R which can be run to generate processed_data.csv. This can also be done using the shell script run_preprocess.sh. The code for the analysis may be found in Q2ImportantVariables.Rmd.

Specifically to address the question, we first processed the dataset to remove or impute NAs depending on the numbers of features missing in the observation. Additionally, any redundant columns and traits that closely correlated with one another or with the response variable where removed from the dataset. The correlation heat map checks for any correlation between the variables. Variations of PCA bivariate plots were constructed to see if any groupings or trends can be observed when labeling the data points with Ratio of CH to CL variable. To then address the questions, the Ratio of CH to CL variable was converted to a binary variable with a threshold of 1 to categorize the plots based on whether they had a majority of selfing plants or cross pollination plants. With this binary response variable, a support vector classifier was built to train and test on the dataset. Moreover, to produce more interpretable results, a decision tree was constructed. To extend from that, a random forest model was also built with k-fold cross validation.

Q3. Can we identify the most important variables that influence plant reproductive success and use them to develop a decision tree that can guide plant breeding efforts?

The remainder of the analysis may be found in RVtrees.Rmd. The analysis involves removing and imputing NAs and transforming the response variable to binary based on a average threshold on the mean seed mass of the plots. The average seed mass for CH plants was removed from the dataset due to high amount of NAs, so the remainder of the analysis was done just considering the CL plants. A decision tree was constructed to evaluate which variables are best to split on based on information gain.
