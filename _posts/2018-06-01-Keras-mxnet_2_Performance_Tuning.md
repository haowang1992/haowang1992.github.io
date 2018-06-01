---
title: 'Keras-mxnet -- (2) Performance Tuning'
date: 2018-06-01
permalink: /posts/2018/06/Keras-mxnet_Tutorail_2_Performance_Tuning/
tags:
  - Keras Mxnet
  - Performance Tuning
---


# Table of Contents

1. [Channel First Imgae Data Format for CNN](#1-config-channel-first-image-data-format-for-cnn)
2. [Installing Optimized MXNet Binaries](#2-install-optimized-mxnet)
3. [Using MXNet Profiler](#3-mxnet-profiler)


## 1 Config Channle First Image Data Format for CNN

Modify the ~/.keras.json and setting are:

```json
   backend: mxnet
   image_data_format: channels_first
```
Channles_first is optimal for training on NVIDIA GPUs with cuDNN.

NOTE: It is recommended pratice to pass the input_shape based on the shape field of your input tensor (that means first non-input layer).

## 2 Install Optimized MXNet

```bash
   $ pip install mxnet-cu80mkl/mxnet-cu90mkl/mxnet-mkl
```

## 3 Using MXNet Profiler

MXNet (V0.9.1+) has a build-in profiler that gives detailed information about execution time  at the symbol level. This feature complements general profiling tools
like nvprof and gprof by summarizing at the operator level, instead of a function, kernel, or instruction level.


Speed Up!
