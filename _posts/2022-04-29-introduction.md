---
title: "Tutorial Proposal: Visual Fusion for Pattern Recognition"
layout: post
---

Authors: Xiao-Jun Wu, Tianyang Xu, Hui Li, Xiaoqing Luo, Josef Kittler


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




Check out the [Jekyll docs][jekyll-docs] for more info on how to get the most out of Jekyll. File all bugs/feature requests at [Jekyll’s GitHub repo][jekyll-gh]. If you have questions, you can ask them on [Jekyll Talk][jekyll-talk].

[jekyll-docs]: http://jekyllrb.com/docs/home
[jekyll-gh]:   https://github.com/jekyll/jekyll
[jekyll-talk]: https://talk.jekyllrb.com/
