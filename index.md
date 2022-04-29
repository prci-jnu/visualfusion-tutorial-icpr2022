---
title: "Tutorial Proposal: Visual Fusion for Pattern Recognition"
layout: post
---

<h3>Authors: Xiao-Jun Wu, Tianyang Xu, Hui Li, Xiaoqing Luo, Josef Kittler</h3>


# Introduction

Visual fusion plays a pivotal role in pattern recognition, since the single modality (view) only focuses on the local features and can not handle the overall information. With the rise of different types of sensors, the research object of many computer vision tasks changed from a single modality (RGB) to multi modalities which include infrared (thermal or near) information, depth information (depth camera), hyperspectral image (satellite) and LIDAR information. 
These multi-modal data show the urgent need for visual fusion theory in real-world scenarios.

Thus, the use of visual fusion approaches has being an important new trend in several application areas, such as military object detection, civilian security, and construction of smart cities etc. For the areas of academic research, visual information fusion can be applied to many computer vision tasks, such as object tracking, semantic segmentation, 3D reconstruction and text-image generation etc. To this end, the visual fusion approaches not only require achieving better fusion performance, but also have to guarantee the generalisation power.

All these above conditions make visual information fusion studies become a crucial research field, covering the following topics: a) Research on visual information fusion algorithms, including machine learning (without deep learning) based methods and deep learning-based networks; b) Research on quality evaluation of visual fusion results which is a key issue for visual information fusion, include reference metrics and no-reference metrics; c) Research on applications of visual fusion algorithms, which denotes the practical application value of visual fusion studies. 

To this end, the tutorial will offer a) an overview of all the above plus other related topics and will stress the related algorithmic aspects, such as: b) Visual fusion frameworks, which contain the visual fusion methods and the performance evaluation; c) Image fusion techniques, which mainly introduced the deep learning-based fusion networks; d) Visual fusion applications.



# Topics

### Visual fusion basics 
In the era of knowledge explosion, the attention to visual fusion technology has proliferated due to the significant development and availability of different kinds of sensor devices. 

Visual fusion is an important branch of information fusion that originated in the mid-1980s, which attempts to simulate biological perception and cognitive processes of objective reality. The pipeline of the visual fusion system contains four parts: spatiotemporal registration, data preprocessing, data fusion, and data post-processing. Among these, the phase of data fusion is the primary concern, where the useful information from visual sources captured in the same scene is extracted and combined into a compact form of visual information representation, which leads to a more comprehensive, more robust, less redundant and less uncertain system \cite{li2013image}. 

In the last few decades, both conventional methods like multi-scale analysis and the advanced technologies of deep learning have gained breakthroughs in visual fusion tasks. Researchers concluded three basic principles in visual fusion through long-term practise: (1) the fused visual data should contain all the salient information from multi-modal sources; (2) no artificial information can be introduced; (3) Information that is not of interest, e.g. noise, should be suppressed as much as possible. 

Visual fusion makes full use of the complementary and redundant information among multi-modal data \cite{li2017pixel}\cite{ma2019infrared}. Thereby, different from the broad sense of visual enhancement, it is more like the kind of technology in the field of visual understanding, which constructs compact data that is appropriate and understandable for not only human observers, but also facilitates the subsequent processing and perception of the machine. Due to such characteristics, visual fusion is becoming a critical topic in the pattern recognition community. The widely investigated applications of visual fusion include daily monitoring, medical diagnosis, security check and autonomous driving.} 


### Visual fusion frameworks

he study of visual fusion is made up of two important aspects: the visual fusion methods and performance evaluation. 
According to the different processing stages for fusion, visual fusion can be classified into three categories: data-level fusion, feature-level fusion and decision-level fusion. Data-level fusion directly performs the fusion process on the raw data sources. 

Then, feature extraction and decision-making are performed on the obtained fused data. It is the basic fusion model with less loss of information and is widely investigated in the community. Typical frameworks include the multi-scale transform, sparse representation, sub-space, deep learning and hybrid. For all of them, whether explicit or implicit, the fusion process can be generally concluded as four steps: (1) transform the source data into a different representation; (2) extract the features from the representations to measure the activity level; (3) design the specific fusion rule; (4) inversely transform the fused representation into the fused result.

Feature-level fusion is conducted on the feature vectors, which are able to compress the considerable data amount, facilitating the real-time processing. Common methods contain the K- nearest neighbour, cluster compression, neural network and so on. 
Decision-level fusion is conducted at the highest abstraction level, fusing the decisions made by each sensor in the fusion centre, which is directly targeted at the decision objectives. Such processing methods are of the lowest precision, but are robust to interference with low computation cost. Dempster-Shafer evidence theory, Bayesian estimation and expert system are representative frameworks for decision-level fusion. After achieving the fused results, performance evaluation should be conducted in a subjective and objective way. 

Subjective methods assess the fused quality based on the human visual system, which is intuitive but easily biased by observers. 
Objective methods quantify the fused quality using various mathematical tools like statistics, information theory, gradients, etc. 
The adopted evaluation methods will vary according to the specific tasks, \textit{e.g.}, object recognition and classification.} 


### Image fusion techniques

The main purpose of image fusion is to generate a single composite image that contains more complementary features and reduces redundant information from multi-modal source images. Ideally, the fusion algorithm can preserve more useful information into the final fused image, which is a benefit for the downstream computer vision tasks. 

The image fusion techniques can be broadly separated into two categories: (1) non-deep learning based fusion methods; (2) deep learning based fusion methods. From the general representation learning based fusion methods (multi-scale transform, sparse/low-rank representation)\cite{li2017multi}\cite{li2020mdlatlrr} to the hybrid fusion algorithms (Morphological Analysis, Pulse-coupled neural networks etc.)\cite{luo2016image}\cite{Zhang2016boundary}\cite{yin2018medical}, these methods reflect the continued research enthusiasm for image fusion task. 

Moreover, with the learning mechanism (deep learning), it injects new vitality into the image fusion research\cite{liu2017multi}\cite{li2018densefuse}\cite{li2018infrared}\cite{li2021rfn}\cite{luo2021latraivf}. 
The design complexities of feature extraction and fusion strategy can be reduced, which allows us to design the network architecture for the specific image fusion task. In this topic, we mainly introduce deep learning-based image fusion techniques.

For deep learning-based fusion networks, they can be categorized into three classes: (1) Pre-trained network-based fusion framework; (2) Auto-encoder based fusion framework; (3) End-to-end network-based fusion framework. In a pre-trained network-based framework, the pre-trained neural networks are utilized to extract the deep features from source images. Then, the appropriate fusion strategies are designed to calculate the fusion weights based on the extracted deep features\cite{li2018infrared}\cite{li2019infrared}. 
For the auto-encoder based fusion model, the encoder and the decoder are utilized to extract features and generate the fused image, which the network architecture can be designed for different fusion asks\cite{li2018densefuse}\cite{li2020nestfuse}\cite{luo2021ifsepr}. In the end-to-end network-based fusion framework, all the image fusion processes are replaced by a specifically designed fusion network. With the appropriate architecture and the carefully designed loss functions, it can achieve better fusion performance\cite{xu2020u2fusion}\cite{li2021rfn}\cite{luo2021latraivf}.


### Visual fusion applications

Visual fusion has obtained wide attention in many pattern recognition applications. In this section, we will deliver its typical applications, \textit{i.e.}, RGB-T tracking and RGB-D tracking.

In particular, visual object tracking is a fundamental research topic in visual systems. With the access of more sensors, \textit{e.g.}, infrared thermal camera and depth camera, recent visual tracking research is focusing on the complementary fusion approach for RGB-T tracking and RGB-D tracking, supplementing the RGB-only appearance models. In consistent with the visual fusion categories, we deliver the RGB-T and RGB-D fusion strategies in input-level fusion, feature-level fusion, and decision-level fusion.
Detailed analysis and performance comparison is discussed for both hand-crafted algorithms and deep networks. We also report the potential of RGB-T and RGB-D fusion research in recent academic competitions\cite{kristan2020eighth}.


# Target Audience

This tutorial contains dedicated basics and recent advances in the visual fusion topic, providing a reference for relevant research topics in pattern recognition, \textit{e.g.}, multi-modal recognition, multi-sensor detection, and multi-device imaging. Related academic students, researchers, and product engineers working in the fields of computer vision and pattern recognition and showing interest in the current development of visual fusion are welcome to attend this tutorial. Specialists from different areas who need to integrate the knowledge of visual fusion into their applications are also targeted audiences. The tutorial assumes the most basic knowledge of digital visual data and mathematics. 

Nowadays, we are living in a world with an explosion of multi-modal data. Single-modal data is not sufficient for artificial intelligence to understand the inherent structure and content of the perceived world, thereby degrading their ability to provide a reliable decision. As one of the most important compositions of information, visual processing goes across many scientific fields and much more attention has been put on multi-modal visual fusion. Several visual fusion frameworks are constantly emerging, bringing great achievements in application scenes like object recognition and are conducive to developing intelligent systems that can think and make decisions like a human. To decide which fusion method is of higher performance, the quantitative and qualitative evaluation should be conducted in a systematic way. Thus, this tutorial aims to give a comprehensive introduction to the theory of visual fusion and its significance in pattern recognition, as well as a thorough overview of the commonly accepted visual fusion techniques with their evaluation methods, which may be helpful for researchers to better understand the concept of visual fusion, then some inspirations may be derived about the potential research directions.


# Organisers

Xiao-Jun Wu (wu_xiaojun@jiangnan.edu.cn), Professor in the School of Artificial Intelligence and Computer Science at Jiangnan University, Wuxi, China. His research interests include pattern recognition, computer vision, fuzzy systems, neural networks and intelligent systems.
Tianyang Xu (tianyang.xu@jiangnan.edu.cn), Associate Professor at the School of Artificial Intelligence and Computer Science, Jiangnan University, Wuxi, China.
His research interests include visual tracking and deep learning. 

Hui Li (lihui.cv@jiangnan.edu.cn), Lecturer at the School of Artificial Intelligence and Computer Science, Jiangnan University, Wuxi, China. His research interests include image fusion, and deep learning. 

Xiaoqing Luo (xqluo@jiangnan.edu.cn), Associate Professor at the School of Artificial Intelligence and Computer Science, Jiangnan University, Wuxi, China. Her research interests include image fusion, pattern recognition, and other problems in image technologies.

Josef Kittler (j.kittler@surrey.ac.uk), Distinguished Professor of Machine Intelligence at the Centre for Vision, Speech and Signal Processing, University of Surrey, Guildford, U.K. He conducts research in biometrics, video and image database retrieval, medical image analysis, and cognitive vision. He published the textbook Pattern Recognition: A Statistical Approach and about 1000 scientific papers. His publications have been cited by around 70,000 times. He is series editor of Springer Lecture Notes on Computer Science. He currently serves on the Editorial Boards of Pattern Recognition Letters, Pattern Recognition and Artificial Intelligence, Pattern Analysis and Applications. He also served as a member of the Editorial Board of IEEE Transactions on Pattern Analysis and Machine Intelligence during 1982-1985. He served on the Governing Board of the International Association for Pattern Recognition (IAPR) as one of the two British representatives during 1982-2005, and the President of IAPR during 1994-1996.


# Contact and Preference

Lead organiser: Xiao-Jun Wu, E-mali: wu_xiaojun@jiangnan.edu.cn

Preference: Half-day On-line tutorial



<!-- Check out the [Jekyll docs][jekyll-docs] for more info on how to get the most out of Jekyll. File all bugs/feature requests at [Jekyll’s GitHub repo][jekyll-gh]. If you have questions, you can ask them on [Jekyll Talk][jekyll-talk].

[jekyll-docs]: http://jekyllrb.com/docs/home
[jekyll-gh]:   https://github.com/jekyll/jekyll
[jekyll-talk]: https://talk.jekyllrb.com/ -->
