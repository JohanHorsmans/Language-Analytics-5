# Language-Analytics-5

### Intro

We have chosen the OffensEval2020 dataset containing 3000+ Danish comments from Ekstra Bladet and Reddit, labeled with a binary coding scheme indicating offensiveness (link: https://figshare.com/articles/dataset/Danish_Hate_Speech_Abusive_Language_data/12220805).

OffensEval2020 was a competition where researchers and data scientists from all over the world competed to create the best classification models for various languages (including Danish). 

The best team in the Danish task achieved a macro F1-score of 0.8119 and the worst team achieved a score of 0.4913. For the full paper, see: https://arxiv.org/pdf/2006.07235.pdf

We wanted to create a text classifier that could classify offensive comments in Danish and compare our macro F1-score with the results from the OffensEval2020 competition.

We trained the following models: Logistic Regression, Support Vector Machine, Neural Network, Random Forest & Decision Tree (see code for further specifications). We also combined them in an ensemble where a mix of majority vote- and average ensembling was employed (see code for specifications).

Our best performing model was our ensemble containing all models, which achieved a macro F1-score of 0.71. It is important to note that the dataset is heavily skewed towards non-offensive comments, so the F1-score should be taken with a grain of salt. Nonetheless it would have ranked as the 23rd best model (out of 38) in the OffensEval2020 competition, so we deem it to be quite successful when taking the circumstances into account.


### To run the code, please follow the following steps from the commandline:
1. Clone the reposioty to a folder of your choice on worker02: 
- cd {folder of you choice}
- git clone https://github.com/JohanHorsmans/Language-Analytics-5
2. Set your working directory to the newly created repository:
- cd Language-Analytics-5
3. Create virtual environment: 
- bash hate_env.sh 
5. Activate the enviroment:
- source hate_env/bin/activate
6.  run the script: 
- python HateClass.py
