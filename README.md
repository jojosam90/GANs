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


































