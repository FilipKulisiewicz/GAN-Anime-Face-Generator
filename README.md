# GAN-Anime-Face-Generator

1. Introduction:
Generative Adversarial Networks (GANs) are a class of deep learning models that are used to generate new data samples that are similar to a given training set. GANs consist of two main components: a generator network, which is responsible for generating new samples, and a discriminator network, which is responsible for determining whether a given sample is real or fake. The generator and discriminator are trained simultaneously, with the generator trying to produce samples that can “fool” the discriminator, and the discriminator trying to correctly identify real and fake samples. 
2. Method:
 In this project, we aim to train a GAN to generate anime faces. The architecture of the GAN model used in this project is composed of a deep convolutional generator network and a deep convolutional discriminator network. The dataset used to train the GAN is a collection of 36.7k anime face images.
3.  Experimental details:
 During training, we alternated between training the discriminator and the generator. The real_loss and fake_loss functions were used to calculate the discriminator losses. The generator was trained with the aim of tricking the discriminator and had an opposing loss function. We used the Adam optimizer to train the GAN with a learning rate of 0.0002, betas (0.5, 0.999) and a batch size of 128. We trained the GAN for a total of 40 epochs. 
4. Personal Views:
To improve the performance of GANs, methods like increasing the model size and number of epochs also checking different optimizers, should be consider as generated samples highly depend on used parameters like number of epochs, loss function, type of optimizer and it's  hyperparameter.

5. Effect: 
5.1. Generated faces after 1 epoch

![image](https://user-images.githubusercontent.com/73996991/226204422-faa996fd-8d29-475a-b030-2addc7144f89.png)

5.2.  Generated faces 40 epochs

![image](https://user-images.githubusercontent.com/73996991/226204432-95a578ba-6c80-49b0-a286-527ed59a9b61.png)

5.3. Training Losses

![image](https://user-images.githubusercontent.com/73996991/226204437-a4ad6305-7b90-4881-8419-7aaad1cc972d.png)


Plotted data clearly shows that the losses are fluctuating what suggests that both the generator and the discriminator are making progress during training. High jumps of discrimination loss means a harder time distinguishing the images, which is an indication that the generator is improving. It's also visible that most of the times the generator loss jump preceded by the decrease in the discriminator loss what may indicate that the discriminator just 'learn' new feature. 
