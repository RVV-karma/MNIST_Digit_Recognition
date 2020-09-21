# MNIST_Digit_Recognition
CNN Model to recognize Digits from Images from MNIST Data with accuracy of **99.46%**.  
MNIST Digit Recognition dataset is a great dataset with 60000 training examples and 10000 testing examples.  

## CNN Model
I have used a sequential model with following layers in order:  
1. 2D Convolution Layer with 32 filters and 3x3 kernal size.  
2. 2D Maximum Pooling Layer with 2x2 kernal size.  
3. 2D Convolution Layer with 64 filters and 2x2 kernal size.  
4. 2D Maximum Pooling Layer with 2x2 kernal size.  
5. 2D Convolution Layer with 256 filters and 2x2 kernal size.  
6. Flatten Layer.  
7. Dense Layer with 1024 neurons (activation units).  
8. Dense Layer with 256 neurons (activation units).  
9. Dense Layer with 10 neurons (activation units). This is the output layer.  

The optimizer used is Stochastic Gradient Descent (SGD) with learning rate of 0.01 and momentum of 0.9.  
I have trained it on Google Colab for 30 epochs with a batch size of 32.  

## Conclusions
1. CNN Model is good to start with, for image recognition.  
2. Keras is great, easy-to-use library for implementing neural networks.  
3. Since the training accuracy is 1.0000 but test accuracy is 0.99460, so the model can be inproved by increasing its depth/ adding more layers. The little problem is high variance. (I will try to improve it.)  
4. I have trained the model using both GPU and TPU, and found that, TPU is faster for higher batch sizes(>256) whereas GPU is faster for lower batch sizes.  
