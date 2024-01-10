
# A Convolutional Neural Network (CNN)

What is mean by Convolution?

* The first layer is employed to extract diverse features from input images.
* In this layer, the mathematical operation of convolution is performed between the input image and a filter of a particular size MxM.
* During the process of sliding the filter over the input image, the dot product is computed by comparing the filter with different sections of the input image, and this calculation is adjusted according to the dimensions of the filter (MxM).
* The output, termed the Feature Map, provides information about image features such as corners and edges.
* The Feature Map is then passed to subsequent layers to learn additional features of the input image.





## CNN Architecture

![App Screenshot](https://editor.analyticsvidhya.com/uploads/59954intro%20to%20CNN.JPG)



**Convolution of a 5x5 input with a 3x3 kernel**

![App Screenshot](https://github.com/prodramp/python-projects/blob/main/images/5x5-cov.png?raw=true)

![App Screenshot](https://www.researchgate.net/publication/348296106/figure/fig2/AS:977241114681348@1610003846772/Example-of-Convolutional-layer.ppm)

**Step-by-step of the convolution of a 5x5 image with a 3x3 kernel**

![App Screenshot](https://miro.medium.com/v2/resize:fit:1200/0*eqdnS06UbtxxYec3.gif)

![App Screenshot](https://github.com/prodramp/python-projects/blob/main/images/5x5-img-conv-3x3kernel.png?raw=true)
## Pooling

* Two main elements 

1. Pooling size (x,y )
2. Stride



* The primary aim of this layer is to decrease the size of the convolved feature map to reduce computational costs.

* This is performed by decreasing the connections between layers and independently operating on each feature map.

* It is a downsampling operation executed over each feature map.

* It extracts receptive fields from the feature map and replaces it with a single value.

* This single value can be obtained by different aggregation criteria, such as maximum value, average, or weighted average according to the distance from the centre of the receptive field.

* In Max Pooling, the largest element is taken from the feature map.

* Average Pooling calculates the average of the elements in a predefined sized Image section.

* The total sum of the elements in the predefined section is computed in Sum Pooling.

* The Pooling Layer usually serves as a bridge between the Convolutional Layer and the FC Layer

![App Screenshot](https://miro.medium.com/v2/resize:fit:679/1*fXxDBsJ96FKEtMOa9vNgjA.gif)


## Flatten



* Take x,y,z dimension and convert them to xyz

* Convert (100,100,1) => 1000

## Dropout



* Usage - Dropout(0.2) - 20% of the values randomly set to 0
* The Dropout layer randomly sets input units to 0 with a frequency of rate at each step during training time, which helps prevent overfitting.
* Dropout is commonly used to regularize deep neural networks; however, applying dropout on fully-connected layers and applying dropout on convolutional layers are fundamentally different operations.
* The Dropout layer randomly sets input units to 0 with a frequency of rate at each step during training time, which helps prevent overfitting.
* Dropout(0.5) means - creating a dropout layer with a 50% chance of setting inputs to zero.

![App Screenshot](https://www.oreilly.com/api/v2/epubs/9781788295628/files/assets/d4d20bd7-192c-48e7-9da2-6d3ddc7929e7.png)
## References



* https://medium.com/aiguys/deep-convolutional-neural-networks-dcnns-explained-in-layman-terms-b990b2818061

* https://towardsdatascience.com/dropout-on-convolutional-layers-is-weird-5c6ab14f19b2

* https://www.cs.ryerson.ca/~aharley/vis/conv/flat.html

* https://towardsdatascience.com/visualizing-the-fundamentals-of-convolutional-neural-networks-6021e5b07f69

* https://github.com/prodramp/python-projects/tree/main/deeplearning/cnn

* https://github.com/christianversloot/machine-learning-articles/blob/main/how-to-predict-new-samples-with-your-keras-model.md
# deeplearning-cnn
