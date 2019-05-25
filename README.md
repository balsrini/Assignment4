# Architectural Basics

1. 3x3 Convolutions,

   ​	We know for sure that 3x3 kernels are to be used and hence i plan to use the 3x3 kernels as they can find edges better than even x even kernels

2. Receptive Field,

   ​	The image database we have is the the mnist and from the matlab plot it seems most of the objects are in the center of the image. Typically objects are starting at 5px and ending at 23 pixels.

3. Kernels and how do we decide the number of kernels?

   ​	I started with 16 kernels since we need only 10 classifications and gradually increased the kernels.

4. SoftMax,

   ​	We are using softmax to predict the outcome. Before the softmax, i am not doing relu activation in order to assist softmax in better prediction

5. MaxPooling,

   ​

6. Position of MaxPooling,

7. The distance of MaxPooling from Prediction,

8. How many layers,

9. 1x1 Convolutions,

10. Concept of Transition Layers,

11. Position of Transition Layer,

12. Learning Rate,

13. Batch Normalization,

14. The distance of Batch Normalization from Prediction,

15. DropOut

16. When do we introduce DropOut, or when do we know we have some overfitting

17. Number of Epochs and when to increase them,

18. When do we stop convolutions and go ahead with a larger kernel or some other alternative (which we have not yet covered)

19. How do we know our network is not going well, comparatively, very early

20. Batch Size, and effects of batch size

21. LR schedule and concept behind it

22. When to add validation checks

23. Adam vs SGD

24. Image Normalization,

    ​