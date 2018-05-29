---
title: 'Keras-mxnet -- (1) Installation and Validation'
date: 2018-05-29
permalink: /posts/2018/05/Keras-mxnet_Tutorail_1_Installation_and_Validation/
tags:
  - Keras
  - Mxnet Backend
  - Installation and Validation
---

Keras is a high-level neural networks API in Python and capable of running on the top of Tensorflow, CNTK, Theano or Mxnet. It was developed with a focus on enabling fast experimentation. Bing able to go from idea to result with the least possible delay is key to doing good research. -- from [Keras.io](https://keras.io/)


# Table of Contents

1. [Install Keras with Apache MXNet backend](#1-install-keras-with-apache-mxnet-backend)  
2. [Train MNIST classification model](#2-train-mnist-classification-model)  


## 1 Install Keras with Apache MXNet backend

```bash
   $ pip/pip3 install h5py graphviz pydot --user
   $ pip/pip3 install mxnet-mkl --user
   $ pip/pip3 install keras-mxnet --user
```

When the Keras-mxnet and MXNet is installed, modify the ~/.keras.json and setting are:

```json
   backend: mxnet
   image_data_format: channel_first
```

Then we validation the installation by:

```bash
   $python
   >>> import keras as K
       Using mxnet backend
```

## 2 Train MNIST Classification Model   

```
Using MXNet backend
Downloading data from [https://s3.amazonaws.com/img-datasets/mnist.npz](https://s3.amazonaws.com/img-datasets/mnist.npz)  
... ...  
60000 train samples

10000 test samples

_________________________________________________________________

Layer (type)                 Output Shape              Param #   

=================================================================

dense_1 (Dense)              (None, 512)               401920    
_________________________________________________________________

dropout_1 (Dropout)          (None, 512)               0         
_________________________________________________________________

dense_2 (Dense)              (None, 512)               262656    
_________________________________________________________________

dropout_2 (Dropout)          (None, 512)               0         
_________________________________________________________________

dense_3 (Dense)              (None, 10)                5130      
  
=================================================================  
Total params: 669,706  
Trainable params: 669,706  
Non-trainable params: 0  
________________________________________________________________  
Train on 60000 samples, validate on 10000 samples  
```

Congratulations! You are using Keras with MXNet as backend!  
