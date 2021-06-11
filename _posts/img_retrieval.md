---
title: "[Paper Review] Particular Object Retrieval with Integral Max-pooling of CNN Activations"
excerpt: "How to extract features from an image?"
date: 2021-05-15 01:000 -0400
use_math: true
tags :
- image retrieval
- paper review

category: [CV]



---



기존 방식

content based image retrieval.

Bag-of-Words model을 사용.

이런거는 보통 filtering stage를 만들어서 image를 similarity에 따라 ranking

하고 re-ranking으로 top n 을 쳐내는 식으로

지금(15년)은 CNN 기반. hidden status를 feature vector로 보는것. feature vector? 약간 representations vector from an image 인거야. 똑같이 ranking 들어가고

Step: encode image to get a feature extractor. then employ the generalized mean







# Maximum Activations of Convolutions (MAC)

pre-trained CNN and discarding all the FC layers

Given an input image I of size $W_I \times H_I$, the activations (responses) of a convolutional layer form a 3D tensor of $W × H × K$ dimensions, where $K$ is the number of output feature channels.



**max-pooling** operated over a single region of size W × H.

Unlike FC layers, max-pooling would miss geometric details 

It encodes the maximum “local” response of each of the convolutional filters and is therefore translation invariant



# R-MAC: regional maximum activation of convolutions

Consider a set of $R$ regions of different size on the CNN response maps

calculate the feature vector for each region, 

combine the collection of regional feature vecctors into a single image vector

same dimensionality but better performance







# Object Localization

Initial ranking stage, not using all K-sized vectors but trimming less similar regions then calculate similarities in left regions again.

; not the similarity between the query image and the whole image, but the one between the query image and the most similar region $R'$, being selected from a set of $R$. 

## Approximate integral max-pooling

di






## Reference

- https://arxiv.org/pdf/1511.05879v1.pdf