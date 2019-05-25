# Architectural Basics

1. 3x3 Convolutions,

   ​	We know for sure that 3x3 kernels are to be used and hence i plan to use the 3x3 kernels as they can find edges better than even x even kernels

2. Receptive Field,

   ​	The image database we have is the the mnist and from the matlab plot it seems most of the objects are in the center of the image. Typically objects are starting at 5px and ending at 23 pixels.

3. Kernels and how do we decide the number of kernels?

   ​	I started with 16 kernels since we need only 10 classifications and gradually increased the number of kernels. This got me more number of parameters.

4. SoftMax,

   ​	i am using softmax to predict the outcome. Before the softmax, i am not doing relu activation in order to assist softmax in better prediction

5. MaxPooling,

   ​	I need to reduce the size of the image at the early stage to reduce the parameters.

   I am using Maxpooling as the 4 layer to make sure we can see the edges after the first 3 convolutions. This will help reduce the size of the image. 

6. Position of MaxPooling,

   ​	I am using Maxpooling only once after 3 convolutions as it is small object of approx size 20 pixels and using it twice might not yield accuracy

7. The distance of MaxPooling from Prediction,

   ​	In the image of approx 20pixels, at the last layer i am not using it as it will hide the facts while predicting.

8. How many layers,

   ​	I am looking at 3 Convolution blocks and trying to fit in the parameters to a limit. Currently i have 3 convolution blocks with 2 transition layer.

9. 1x1 Convolutions,

   ​	Using this convolution to reduce the number of channels. I am using this in my first architecture to reduce the parameters. Typically used after max pooling 

10. Concept of Transition Layers,

    ​	Using the transition layer twice to better train the network and reduce the parameters.

11. Position of Transition Layer,

    ​	The second Transition layer i have will not have max pooling as the RF itself is very small.

12. Batch Normalization,

    ​	The Batch normalization helps to normalize the image which is what i am using in my second notebook.

13. The distance of Batch Normalization from Prediction,

    ​	We have to use the BN after/before convolution but not before the Prediction. As BN will influence the accuracy.

14. DropOut

    ​	Dropout will at random stop few kernels from participating so that the weights can be adjusted during backpropagation.

15. When do we introduce DropOut, or when do we know we have some overfitting

    ​	Using drop out in the third exercise to improve the difference between the training accuracy and the validation accuracy

16. Number of Epochs and when to increase them,

    ​	Started to increase the number of epochs in the fourth stage to gain better accuracy. The number of parameters now are within limits and hence trying out the epochs with learning rate

17. When do we stop convolutions and go ahead with a larger kernel or some other alternative (which we have not yet covered)

18. How do we know our network is not going well, comparatively, very early

    ​	When the desired accuracy is met with the parameters and there is no underfitting or overfitting.

19. Batch Size, and effects of batch size

    The batch size increases the accuracy to an extent but after that the value is almost stable. Random trials i have to take to find the batch size .

20. Learning Rate,

    The learning rate is the ratio that helps to adjust the weights of the kernel. Higher learning rate will cause a different minima to be found. Hence the LR should be adjusted very slowly .

21. LR schedule and concept behind it

    In my fourth assignment i have reduced the LR and increased the epoch so that we can find the minima faster.

22. When to add validation checks

    ​	Once we have got the defined accuracy, we need the validation checks to determine if we are overfitting or underfitting. At the end of finalizing the network, we need to add the validation checks

23. Adam vs SGD

     Used Adam as it is a good optimization algorithm and has provided good accuracy compared to SGD. Adam is derived from adaptive moment estimation.

24. Image Normalization

    In the process of exploring the kinds of Image normalization.

    ​