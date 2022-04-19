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

