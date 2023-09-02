# Stability-of-Different-types-of-GANs
In this assignment, we implemented three types of Generative Adversarial Networks (GAN), including Deep Convolutional GAN (DC-GAN), Auxiliary Conditional GAN (AC-GAN) and Wasserstein GAN (WGAN), on a dataset containing binary finger images. In terms of DC-GAN, we utilized different preprocessing techniques, such as smoothing labels and adding noise, to increase the stability of the model and thus good quality images generated. As can be seen below, the original DC-GAN have a divergent trend in its loss function in which loss of generator is increasing, while by using these two techniques the convergence is improved, especially when smooth labels are used.

![DCGAN](https://github.com/ErshadHasanpour/Stability-of-Different-types-of-GANs/assets/96794427/98bd30b8-acba-4573-ab57-c6cf05d415d2)

With regards to AC-GAN, we used the class number of each image, shown by the number of fingers, as an input in both discriminator and generator. Not only this approach provides us with more control over which class of images we want to generate, but also stabilizes the training process. Left image below shows that the stability of training is much better improved compared to previous techniques. The right image illustrates four generated finger images showing number 4 since we asked the model to give us images of this specific class. 

![ACGAN](https://github.com/ErshadHasanpour/Stability-of-Different-types-of-GANs/assets/96794427/41716850-b0c2-4954-ad94-a53669f25297)
 
As for the WGAN, we utilized the ideas of gradient clipping for regularization and Wasserstein loss for scoring fake and real images rather than classifying them. These ideas can improve the stability of the model and the quality of synthetic images. The loss function of WGAN during training is depicted below, in which it can be seen  that convergence has improved in comparison with DC-GAN. 

![WGAN](https://github.com/ErshadHasanpour/Stability-of-Different-types-of-GANs/assets/96794427/24a05db3-1242-4b56-a5b5-d544352ef13f)
