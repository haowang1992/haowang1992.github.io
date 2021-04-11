---
title: "TCN"
collection: publications
permalink: /publication/TCN

excerpt: 'Transferable Coupled Network for Zero-Shot Sketch-Based Image Retrieval'
date: 2021-11-01
venue: 'Submitted to Journal'

---
Transferable Coupled Network for Zero-Shot Sketch-Based Image Retrieval  
# Abstract
Zero-Shot Sketch-Based Image Retrieval (ZS-SBIR) aims at searching corresponding natural 
images with the given free-hand sketches, under the more realistic and challenging scenario 
of Zero-Shot Learning (ZSL). Prior works concentrate much on aligning the sketch and image 
feature representations while ignoring the explicit learning of heterogeneous feature extractors 
to make themselves capable of aligning multi-modal features, with the expense of deteriorating the 
transferability from seen categories to unseen ones. To address this issue, we propose a novel 
Transferable Coupled Network (TCN) to effectively improve network transferability, with the constraint 
of soft weight-sharing among heterogeneous convolutional layers to capture similar geometric patterns, e.g., 
contours of sketches and images. Based on this, we further introduce and validate a general criterion 
to deal with multi-modal zero-shot learning, i.e., utilizing coupled modules for mining modality-common 
knowledge while independent modules for learning modality-specific information. Moreover, we elaborate 
a simple but effective semantic metric to integrate local metric learning and global semantic constraint 
into a unified formula to significantly boost the performance. Extensive experiments on three popular 
large-scale datasets show that our proposed approach outperforms state-of-the-art methods to a remarkable 
extent: by more than 12% on Sketchy, 2% on TUBerlin and 6% on QuickDraw datasets in terms of retrieval 
accuracy. The project page is available at: https://haowang1992.github.io/publication/TCN


---
# Introduction
![image](/files/Submitted2PAMI/intro.png)  
Zero-shot sketch-based image retrieval aims at performing sketch-based image retrieval under the realistic scenario of zero-shot learning  
 
---

---
# Motivation
![image](/files/Submitted2PAMI/moti.png)  
**HWS**: low classification loss, high validation accuracy -> low retrieval performance  
**SWS**: higher classification loss, lower validation accuracy -> higher retrieval performance  

![image](/files/Submitted2PAMI/moti2.png)  
**HWS**: more large singulars in training sketch features than image -> low retrieval performance  
**SWS**: less large singulars in training sketch features than image -> higher retrieval performance  
  
---

---
# Framework
![image](/files/Submitted2PAMI/framework.png)  
Our framework consists of transferable coupled network (i.e., coupled image and sketch encoders), 
feature embedding network, discrimination module and semantic metric module. Specifically, 
the first one includes soft weight-shared convolutional layers (i.e., constrained with <img src="http://www.forkosh.com/mathtex.cgi? \Large \mathcal{L}_{SWS}">) and 
independent batch normalization layers. Retrieval features are obtained through feature embedding network, 
along with discrimination loss <img src="http://www.forkosh.com/mathtex.cgi? \Large \mathcal{L}_{DIS}"> and semantic metric loss <img src="http://www.forkosh.com/mathtex.cgi? \Large \mathcal{L}_{SEM}">. At training stage, 
the guiding signals produced from teacher network as well as benchmark one-hot labels are provided to 
calculate <img src="http://www.forkosh.com/mathtex.cgi? \Large \mathcal{L}_{DIS}">. Similarly, word vectors and uniform noise are offered to compute <img src="http://www.forkosh.com/mathtex.cgi? \Large \mathcal{L}_{SEM}">
  
---
# Result
![image](/files/Submitted2PAMI/res.png)  
![image](/files/Submitted2PAMI/res2.png)  
![image](/files/Submitted2PAMI/res3.png)    
![image](/files/Submitted2PAMI/res4.png)  
  
---
# Download
[[pdf coming soon]](/files/Submitted2PAMI/tcn.pdf)
[[code coming soon]](https://github.com/haowang1992/TCN)


# Concat
Hao Wang: hwang_xidian@163.com

