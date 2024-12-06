# Legal Context and Precedent Mapping 

## Introduction

This repository contains code for our (Jingtian Chen, Srinidhi Narayanan, Anahita Srinivasan) NLP (MIT 6.8610) final project, which proposes novel methods for legal passage retrieval. Key to the project is the LePaRD dataset, which contains 21 million example contexts from court cases along with the cited precedent case and particular quote within. We use a cut of the data (rows corresponding to the top 10,000 cited passages) which can be found here (omitted from repo due to size constraints): https://drive.google.com/file/d/1A02rma5-s_M4UOn7IklAXz6CtpHwoh-g/view?usp=drive_link.


## Method 1: Baseline and Finetuning

The file **hyperparameter_finetuning.ipynb** contains the code for evaluating DistilBERT on the dataset, as well as finetuning DistilBERT, LEGAL-BERT, and LEGAL-BERT-small.  


## Method 2: Two-Step Hierarchical Supervised Classification

The file **hierarchical_supervision_off_the_shelf.ipynb** contains the code for the two-step process that uses an off-the-shelf version of DistilBERT to embed the context and quotations, then uses cosine similarity to select the appropriate quotations.  

The file **hierarchical_supervision_finetuned.ipynb** contains the code for the two-step process that uses a finetuned version of DistilBERT to embed the context and quotations, then uses cosine similarity to select the appropriate quotations.  

The file **hierarchical_supervision_cross_encoder.ipynb** contains the code for the two-step process that uses a cross-encoder to select the closest quotation to a given context.

All three files use the saved weights from a finetuned supervised classification model created using Method 1 that classifies context statements into precedential cases. The saved weights can be found at this link: https://drive.google.com/file/d/1MoQHzW9AVV1q3OuG1Np00_S5k-Blg2EA/view?usp=sharing 


## Method 3: Cross-Encoder

The file **Cross_Encoder.ipynb** contains the code for training and evaluating the DistilRoBERTa cross-encoder.

The saved weights for the cross-encoder can be found at this link: https://drive.google.com/file/d/15vjSb5crYwgkK8Lhuo5LCLE4GJo_CM85/view?usp=sharing
