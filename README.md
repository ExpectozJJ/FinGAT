# Fingerprint-enhanced graph attention network (FinGAT) model for antibiotic discovery
### About

This repository contains all the codes and datasets required to replicate the experiments and analysis in the article "Fingerprint-enhanced graph attention network (FinGAT) model for antibiotic discovery".


The code for this project was written in JupyterNotebook

Installation: https://jupyter.org/install

### Packages required:

Numpy: https://numpy.org/install/

Pandas: https://pandas.pydata.org/docs/getting_started/install.html

Pytorch: https://pytorch.org/get-started/locally/

Pytorch Geometric: https://pytorch-geometric.readthedocs.io/en/latest/notes/installation.html

Scikit-Learn: https://scikit-learn.org/stable/install.html

Chemprop: https://chemprop.readthedocs.io/en/latest/installation.html

RDKit: https://www.rdkit.org/docs/Install.html


### Dataset
##### training_data.csv
Consisted of 2335 molecules represented as thier SMILES notation. Activity column in this dataset is to indicate presence (1) or absence (0) of the molecular property that inhibit against the growth of E. coli.

##### wordvectors.kv
It contains the pretrained word embeddings for tokens of the SMILES strings of the molecules in our dataset. This file will be used in the ablation study experiment. 

##### 5 Fold CV
A folder contains 5 splits (or folds) of training and test sets for 5 fold cross validation. These 5 folds of data will be used in the model evaluations for the our proposed model and the competing GNN models. 

![flowchart](https://user-images.githubusercontent.com/32187437/187708602-27ee23d5-70a4-41e2-a518-0663df03ab0b.png)

### Models

#### Comparison in performance with other existing GNN models
To replicate the experiment for section 4.1 in the articles, we will need 
##### 1_5_evaluation_ECC.ipynb
##### 1_5_evaluation_GraphSAGE.ipynb
##### 1_5_evaluation_Chemprop.ipynb
##### 1_5_evaluation_GAT.ipynb
to obtain the performance metrics for repective models.

### Parameter Tuning 

#### Ablation study
A study in section 4.2 of the article to investigate the contribution of Morgan Fingerprint, molecular graph ebeddings and SMIELS text embeddings towards the molecular property of interest. 
##### Ablation_study.ipynb


#### Effect of sampling proportion of classes
To investigate the effect of ratio of classes in the dataset on the performance of our proposed model.
##### Ratio_GAT_evaluation.ipynb


#### Effect of feed-forward neural network architecture 
To investigate the effect of FNN architecture on the performance of our proposed model.
##### FNN_analysis.ipynb




