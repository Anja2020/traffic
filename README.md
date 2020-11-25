# traffic

While experimenting with different parameters for the model, I realized the impact of different numbers of convolutional and pooling layers. Different numbers of convolutional and pooling layers (e.g. 2 x convolutional layer and 1 x pooling layer) result in a quite bad accuracy and a high loss value. Having two of each with the same number of filters resulted in similarly bad results. Only by increasing the number of filters in the second layers improved the accuracy and the loss by a lot. This shows that the models learning rate is increasing by the process. Adding one more convolutional and pooling layer didn't had an remarkable impact, even with an increased number of filters. 

In respect to the size of the kernel, I achieved the best result with a 6x6 size. Bigger and smaller ones resulted in a quite low accuracy and a quite high loss. Only having one convolutional layer with a 3x3 kernel, the number of filters didn't have a big impact.

For the number of filters and the kernel size in the convolutional layer, I experienced as well, that the numbers have to depend on the size of the image. For some values which were probably to high, I received some errors. 

Regarding the pool sizes of the pooling layers, I realized that the smaller the pool size, the better the accuracy and loss. That's why I chose a (2, 2) pool instead of (4, 4) or (8, 8) which I tried out as well.

After adapting all these parameters, the number of hidden layers didn't really impact the result. There were only slight differences of the performance with different number of hidden layers. Whereas the Dropout highly effected the result. 0.25 gave the best results. Compared to 0.75 as second best and followed by a Dropout of 0.5.

