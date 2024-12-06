# Legal Context and Precedent Mapping 

## Introduction

This repository contains code for our (Jingtian Chen, Srinidhi Narayanan, Anahita Srinivasan) NLP (MIT 6.8610) final project, which proposes novel methods for legal passage retrieval. Key to the project is the LePaRD dataset, which contains 21 million example contexts from court cases along with the cited precedent case and particular quote within. We use a cut of the data (rows corresponding to the top 10,000 cited passages) which can be found here (omitted from repo due to size constraints): https://drive.google.com/file/d/1A02rma5-s_M4UOn7IklAXz6CtpHwoh-g/view?usp=drive_link.


## Method 1: Baseline and Finetuning

The file **hyperparameter_finetuning.ipynb** contains the code for evaluating DistilBERT on the dataset, as well as finetuning DistilBERT, LEGAL-BERT, and LEGAL-BERT-small.  
