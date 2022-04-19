# GANs
## General ideas
GANs consists of a pair of neural networks that fight with each other. 
One is called generator and another one is called discriminator.

![image](https://user-images.githubusercontent.com/77944932/164000097-174508f6-8509-4725-bd2a-a098d0fd38a2.png)

## Build the simplest GANs
![image](https://user-images.githubusercontent.com/77944932/164000669-617e44f3-5962-4154-826f-28f23aa8cedd.png)

## Build the Discriminator
How to tell computer to differentiate between faces and non-faces?

-Faces:  Top Left and Bottom Right have the big values(dark pixels) whereas the other two corners has small values(light pixels).

-Noisy : Any values fall inside (range 0 to 1).

![image](https://user-images.githubusercontent.com/77944932/164001697-d2dc33c1-24ad-4ac0-9a8c-c6ea24e78fb0.png)

Method : Add the two values correspoonding and subtract the values corresponding to other two corners.

![image](https://user-images.githubusercontent.com/77944932/164002134-a9a44709-02d9-4c58-a89e-69cf5e6bf9b6.png)

For faces, the end result value is high and for non-faces, the end result value is low.
Threshold = 1
More than 1: face.
Less than 1 : no face.

![image](https://user-images.githubusercontent.com/77944932/164002991-f142b159-ddd4-443a-9a06-655db76f72be.png)

![image](https://user-images.githubusercontent.com/77944932/164003062-e710e4ee-87b1-4976-ba83-2bb4dcb3ede3.png)

![image](https://user-images.githubusercontent.com/77944932/164003148-672c470a-1b8c-4b55-9e62-b6cb48356059.png)

## Build the Generator

![image](https://user-images.githubusercontent.com/77944932/164003303-5044b33b-e2db-4dd9-8692-de32bbead4f4.png)

![image](https://user-images.githubusercontent.com/77944932/164003750-d81cefbc-77f9-4c03-80d2-3d5728a31331.png)
 
This is a good generator and able to generate the faces as the end value result is high and also the value for top left and bottom right are always big and the values for the corresponding value are smalls.

![image](https://user-images.githubusercontent.com/77944932/164004396-63c66a1e-074e-4917-8511-554edb98df81.png)

![image](https://user-images.githubusercontent.com/77944932/164005383-05ee3b8f-aefa-4ded-b5b4-9361e5bf6b82.png)

![image](https://user-images.githubusercontent.com/77944932/164005474-5f4d6416-c86e-4c39-9340-6ca6fd192165.png)

## The training process : Backpropagation

![image](https://user-images.githubusercontent.com/77944932/164005870-c68da903-9d64-42be-923b-b1f23d075b56.png)

First taking data point and perform forward pass, calculate prediction and calculate error based on log loss, take the derivative of the error based on all weight using chain rule to tell us how much to obtain each weight in order to best decrease the error (gradient descent).
Plot the error and calculate gradient which is the direction of greatest growth and then take a tiny step in the direction of negative of this gradient in order to find new parameter that decrease error as much as possible.

![image](https://user-images.githubusercontent.com/77944932/164006956-650c6227-ba5e-45a8-9954-8e82b93d4910.png)

![image](https://user-images.githubusercontent.com/77944932/164006992-0d69962b-68ec-433b-bd3d-6c225019c042.png)

## Training the generator and discriminator

Set the random z value (between 0 and 1) as input to generator, do a forward pass to obtain some image which is probably face (generated image). Then pass generated images to discriminator to tell is fake or real. Discriminator output probability.

![image](https://user-images.githubusercontent.com/77944932/164008599-32641c97-e177-46c1-a030-d9e74e968443.png)

![image](https://user-images.githubusercontent.com/77944932/164008713-4fc78a3b-7b93-4ffc-a117-950b13ec9b7f.png)

![image](https://user-images.githubusercontent.com/77944932/164008882-f693e0dd-5bc9-4db6-8cf5-2879a1d5c17b.png)




































