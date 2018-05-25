### Convolutional Networks

The increasing depth corresponds roughly to the semantic complexity of the representation.



### Fully Convolutional Network

Fully connected layers do not preserve spatial information.

Fully Convolutional Network (FCNs) preserve the spatial information throughout the entire network.
Since convolutional operations do not care about the size of the input, a fully convolutional network will work on images of any size.

In a classic convolutional network with fully connected final layers, the size of the input is constrained by the size of the fully connected layers.

Fully Convolutional Network special techniques:
* Replacing fully connected layers with one by one convolutional layer
* Up-sampling: Use of transposed convolutional layers
* Connection skipping (information from multiple image scale)

2 major steps:
1. Encoder: extract features from the image
2. Decoder

Examples of Encoder are VGG and ResNet.

### Linear to 1x1 Convolution

Output tensor remains 4D instead of 2D.
The number of kernels is equivalent to the number of outputs in a fully connected layer.
The number of weights in each kernels is equivalent to the number of inputs in the fully connected layer.

### Transposed Convolution (Deconvolution)

Transposed Convolutions help in upsampling the previous layer to a higher resolution or dimension.

### Padding

Convolution as follow

image: input_height * input_width 
filter: filter_height x filter_width
padding in pixels: P

results in 

output: new_height x new_width

We have:

new_height = (input_height - filter_height + 2 * P)/S + 1
new_width = (input_width - filter_width + 2 * P)/S + 1

* "Valid" Padding is no padding.
* "Same" Padding is when the output size is the same as the input size:
=> p = (f - 1)/2

0 = 4 + 2p - f + 1

p = (f - 5) / 2


### Blog Posts

* 📄 [An Intuitive Guide to Deep Network Architectures](https://towardsdatascience.com/an-intuitive-guide-to-deep-network-architectures-65fdc477db41)

* 📄 [Deep Learning for Object Detection: A Comprehensive Review](https://towardsdatascience.com/deep-learning-for-object-detection-a-comprehensive-review-73930816d8d9)