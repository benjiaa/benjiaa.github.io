# My Journey Through Neural Networks: A CS343 Retrospective

*CS343 Was taught in Python. With the exception of the final project, we implemented neural net architectures from scratch barring the use of NumPy for array calculations. The final project involved higher-level functions from Tensorflow to construct models we had already coded by hand. All source files can be found [here](https://github.com/benjiaa/benjiaa-neural-networks)*


Coming back to Colby in the Fall of 2020, I didn’t know what to expect. Classes were online, everyone was scared of COVID, and nobody knew how the year was going to go. If someone had told me then that one of my classes would come to drive my academic interests for the next year and a half (and probably much longer), I am not sure I’d have believed them! Regardless, here is my roundup of the four projects I did in CS343: Neural Networks with Professor Oliver W. Layton. 

## [Project 1:  Single Layer Networks for Binary Classification and Regression](https://github.com/benjiaa/benjiaa-neural-networks/tree/main/project1)
In the first project of the semester, we learned about the basics of neural networks by implementing the ADAptive LInear NEuron (ADALINE) architecture in Python using NumPy. This introduced us to the basic components of neural networks and the functions they serve. While not a particularly complicated task, it was a solid introduction to a neural network with the same building blocks as more complicated architectures that I would learn later on.
Each project consists of implementing a new architecture, then using it to analyze data to perform a task. In project 1, we started by using a dataset about Old Faithful, a geyser in Yellowstone National Park, answering whether the geyser would erupt given certain conditions. ADALINE can also be used for linear regression, as demonstrated in the project as well. As an extension, I created a script implementing ‘one vs the rest’ classification with a binary classifier, turning the number of recognizable classes from 2 into 10 by instantiating the neural net ten times and comparing results. The end accuracy was 86% on the famous MNIST handwriting dataset, which a really satisfying accomplishment!         

### Old faithful Geyser Eruption Classification
![oldfaith](../assets/oldfaith.png)

### Training Plots
![adaline_training](../assets/adaline_training.png)

### Class Boundary visualization                                                                                                           
![oldfaithvis](../assets/oldfaith_vis.png)

## [Project 2: Multilayer Perceptron Networks & The Softmax Layer](https://github.com/benjiaa/benjiaa-neural-networks/tree/main/project2)
In this project, we moved on to implementing a Multilayer Perceptron Network (MLP). The key difference here is the additional hidden layers of neurons between the input and output layers. These more complicated connections allow for the neural network to learn more complex patterns. For example, a single-layer network can only learn linear functions, but a multi-layer network is not bound by this restriction. This is demonstrated with the classic benchmark circle-in-square dataset in the project. 
Another key concept learned in this project is a grid search. Because neural networks can be run with different hyperparameters, it can often be difficult to find best combination of these parameters to minimize training loss. In this project, we were encouraged to explore how performing a grid search can have an impact on performance by attempting to classify the images in the [STL-10 dataset](https://www.tensorflow.org/datasets/catalog/stl10), a well-known image classification data with common photos of various objects. Unfortunately, we only achieved an accuracy of ~30% on the test dataset even after grid searching. (As an extension, I parallelized the grid search process, reducing runtime by a factor of ten!) Visualizations of what the neural net believed each class to “look like”, approximately, are pictured below:

### Class Visualizations
![class_vis](../assets/class_vis.png)

## [Project 3: Convolution and Pooling](https://github.com/benjiaa/benjiaa-neural-networks/tree/main/project3)
In project 3, we implemented a Convolutional Neural Network (CNN). CNNs represented a significant breakthrough at the time of their development, and are notable for their high performance in computer vision tasks. CNNs are typically made of of stacks of convolution and pooling layers that sequentially simplify images throughout the network, allowing the net to more easily recognize important, general patterns without being computationally heavy.
After the arduous process of the by-hand implementation of the CNN, we were able to come back and re-try the STL-10 classification dataset, achieving an accuracy of ~50%! Advancing through this task over the course of projects was satisfying as well as educational.

### Example of a “convolved” Image (above original size)
![convolved](../assets/convolved.png)

### Graph of training over time for the CNN
![train2](../assets/train_2.png)

## [Project 4: Transfer Learning and DeepDream](https://github.com/benjiaa/benjiaa-neural-networks/tree/main/project4)
Finally, after manually implementing these networks, we learned to use high-level Tensorflow functions to build a CNN and attempt classification on a new dataset. Next, utilizing transfer learning, we used a pre-trained neural network (VGG16) to project the receptive fields of specific filters from convolution and and create trippy “dream” effects.  An example of the input and output images is below.

### CNN 'Dreaming' Over a Mountaintop
<img src="../assets/mountain_3x.png" width="200" height="200">
![mdream](../assets/mountain_dream.png)

