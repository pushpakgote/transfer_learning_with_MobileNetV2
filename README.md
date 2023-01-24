# Transfer Learning With MobileNetV2

MobileNetV2 is a convolutional neural network architecture that seeks to perform well on mobile devices. It is based on an inverted residual structure where the residual connections are between the bottleneck layers. The intermediate expansion layer uses lightweight depthwise convolutions to filter features as a source of non-linearity. As a whole, the architecture of MobileNetV2 contains the initial fully convolution layer with 32 filters, followed by 19 residual bottleneck layers.

MobileNetV2 is already trained on many images with 1000+ classes. We can use this trained model according to our needs.

We want to classify images of Alpaca. We can load MobileNet model without its top layers which gives output probabilities of 1000 classes and put our own dense layer with one unit and use binary crossentropy for training.

The training images are preprocessed randomly every time by flipping or rotating and then passing to MobileNet model. We can further fine tune this model by training later layers. 
