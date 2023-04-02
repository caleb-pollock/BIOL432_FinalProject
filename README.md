# BIOL432_FinalProject
Group repository for the final BIOL 432 group assignment for Green Thumbs
Team Name: Green Thumbs
Team Members: Edward Chen, Kerri Lynch, Igor Neder Serafini, Caleb Pollock, Rishona Vemulapalli
Dataset Website: https://zenodo.org/record/5008930
Dataset: https://zenodo.org/record/5008930/files/Soper_Gorden_Adler_AJB_2018_Flower_Insect_Interactions_Processed_Data.csv?download=1

To obtain the data, please download the dataset using the above link. The paper contains multiple dataset which we will not be investigating.

We have 3 questions to address:

Q1. Is it possible to predict the reproductive success of selfing and pollinated plants based on its flower-insect interactions? 

The code for this analysis is located in Q1.Rmd

Q2. Can we determine which variables are important for separating the selfing and pollination mating types?

The preprocessing for the dataset is located in Q2_preprocess.R which can be run to generate processed_data.csv. This can also be done using the shell script run_preprocess.sh. The code for the analysis may be found in Q2ImportantVariables.Rmd.

Can we identify the most important variables that influence plant reproductive success and use them to develop a decision tree that can guide plant breeding efforts?

The remainder of the analysis may be found in RVtrees.Rmd.
