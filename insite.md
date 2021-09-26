---
layout: default
title: "INSITE"
permalink: /insite/
---

# CyberlearningNLP Research @ The Colby INSITE Lab

![poster](../assets/poster.png)

This Summer, I was a research assistant for Professor Stacy A. Doore working on the INSITE Lab’s CyberlearningNLP Project. Personally, I was working on developing an automated accessible STEM image transcription system powered by computer vision and machine learning. This task involves finding a sufficient dataset of chart images to train artificial neural networks on, which is why the International Conference on Pattern Recognition (ICPR 2020) Image Transcription Dataset was chosen for training. This dataset consists of images extracted from open-access publications in the PubMedCentral that have been classified and summarized with descriptions. A subset of this dataset consisting solely of line graphs, bar graphs, pie charts, venn diagrams, and scatter plots was selected for training and testing. This system will consist of four steps: classification, text detection and recognition, text role classification and axis/legend analysis, and NL image description.

Python 3 and Tensorflow/Keras were used to build a convolutional neural network (CNN) for image classification. Projected tasks will likely involve the use of Regional CNNs and Google’s Inception-V2 neural network model. Currently, image classification has been achieved with a 95.888% accuracy after approximately 4 hours of training on an Nvidia Quadro P400 with an image size of 128x128 pixels. The CNN was trained on five classes of the ICPR dataset (n = 12,745). The model was tested on a corresponding dataset (n = 3751). As development continues, researchers will continue to implement the other projected tasks and seek to improve system performance. The final step in the system will be NL image description generation. The ordering, controlled vocabulary, and instructional content of the descriptions created by the system will be based on Fall 2020 and Summer 2021 experiment findings on effective accessible STEM images to optimize BVI student image comprehension and learning outcomes.
