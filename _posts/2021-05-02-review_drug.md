---
title: "Review: Deep Learning in Drug Discovery"
excerpt: "Review basic concepts of drug discovery: Can deep learning accelerate the drug discovery process?"
date: 2021-05-02 01:000 -0400
use_math: true
tags :
- drug discovery
- drug property
- dti
- de novo


---

Drug discovery is $ and time consuming, even taking several years to figure out candidatte chemical compounds for a target. However, thanks to the rise of deep learning, we expect the process to be cheaper and faster! Let's see how we can implement deep learning to the drug discovery problem.

Before we start, there are three ways to represent a drug:

- Molecular fingerprint
- Text-based(SMILES, InChIKey, SELFIES)
- Graph structure



## 1. Drug properties prediction

- Input: A drug (small molecule)
- Output: 0–1 label to indicate whether a drug has certain **properties** or not. (multi-label classification/regression task)



## 2. Drug-Target Interaction Prediction(DTI)

*Point* : Proteins, a very important factor in organs, vary in function depending on its structure, which means that a slight change in protein structure can alter the function of that protein. This transformed protein can have an immediate impact on cells like alleviating pains.

Therefore, whether a given drug can change the protein structure or not is important in drug discovery. DTI measures the interaction between the protein and the drug to figure out drug candidates.

*Goal* : Predict whether a given drug has a relationship with our target protein.

- Description: Binary classification that predicts the binding affinity of compound and protein (it can be formalized as a regression task or binary classification)

- Inputs: Compounds and proteins representation

- Output: 0–1 or a real number in [0–1]

  

## 3. De Novo Drug Design

If we are only interested in compounds with required properties, we can simulate lots of possible chemical structures via **de novo drug design**. You might aware that **generative models** in deep learning, Variational Auto Encoder(VAE) or Generative Adversarial Networks(GAN), can be implemented in this problem. (ex. VAE with SMILES strings.)

Plus, many researchers have combined reinforcement learning for penalizing unideal(unrealistic) molecules and they evaluate their generative models by multiple objects including drug-likeness, toxicity. 





## Reference

- [towardsdatascience posting](https://towardsdatascience.com/review-deep-learning-in-drug-discovery-f4c89e3321e1)