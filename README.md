# Image_Denoising_Autoencoder
## Table Of Contents

- [Dataset](#dataset)
- [Architecture Of Model](#architecture-of-model)
- [Hyperparamters](#hyperparameters)
- [Activation Function](#activation-functions)
- [Loss FUnction and Optimization](#loss-function-and-optimization)
- [Noise Added](#noise-added)
- [Output](#output)

## Dataset:
MNIST dataset used for training a model. 
MNIST contains 60000 training examples and 10000 testing examples.




## Architecture Of Model

Convolutional Neural Network (CNN) used for creating a model. This model contains 6 layers in which 3 are of encoder and 3 of decoder.
For encoder used Conv2d filter and it takes parameter as Con2d(input_channels,output_channels,kernal_size,stride,padding)
For decoder used ConvTranspose2d  filter and it takes parameters as ConvTranspose2d(input_channels,output_channels,kernel_size,stride,padding,output_padding)
 
Model Consists of following sequence of Layers:

Layer 1: Conv2d(1,16,3,stride=2,padding=1)

Layer 2: Conv2d(16,32,3,stride=2,padding=1)

Layer 3: Conv2d(32,64,5)

Layer 4: ConvTranspose2d(64,32,5)

Layer 5: ConvTranspose2d(32,16,3,stride=2,padding=1,output_padding=1)

Layer 6: ConvTranspose2d(16,1,3,stride=2,padding=1,output_padding=1)

## Hyperparameters
Batch Size = 100

Learning rate = 0.001

MSE Loss

ADAM Optimizer

## Activation Functions
ReLU and Sigmoid activation Functions are used to bring non-linearity in model.

## Loss Function and Optimization:
Mean Square Loss (MSE) function is used to calculate loss. 
ADAM Optimizer is used for optimization of model with learning rate 0.001

MNIST:

![image](https://user-images.githubusercontent.com/87741857/136992098-834deea5-3c69-4701-86b1-ed12a16d72e7.png)

FASHIONMNIST:

![image](https://user-images.githubusercontent.com/87741857/137062244-8bf87fc9-d431-46e3-b6cc-270cc7da31c2.png)



## Noise Added
Random noise added via torch.randn() such that we can change noise by changing noise factor. We can also add Gaussin noise,salt noise and many more types of noises.

## OUTPUT
Original Images:

![image](https://user-images.githubusercontent.com/87741857/136761753-307ad2ca-d346-4bb9-8574-a19d193103df.png)


Noisy Images:

![image](https://user-images.githubusercontent.com/87741857/136761600-3dc5d7f7-d0f0-4f1a-8509-8df03ba72a6b.png)


Reconstructed Images:

![image](https://user-images.githubusercontent.com/87741857/136761853-a323de91-977c-4188-8685-84d507b72084.png)

![image](https://user-images.githubusercontent.com/87741857/137062161-737bac83-bca4-4bbb-b6d1-4bcefe954792.png)

![image](https://user-images.githubusercontent.com/87741857/137062177-ad8de0a0-2efe-4bdb-8690-0eaa4e089718.png)

![image](https://user-images.githubusercontent.com/87741857/137062195-ef22e580-303e-49ae-829d-7cc2f7309ade.png)





