# Human Face Generation
> Generation of new, realistic looking faces by DC-GAN trained on celebrity faces

## Table of contents
* [About Project](#about-project)
* [Languages or Frameworks Used](#languages-or-frameworks-used)
* [Setup](#setup)

## About Project:

  The project is about generating new, realistic looking images. I have taken CelebA dataset 
  (you can download [here](https://s3.amazonaws.com/video.udacity-data.com/topher/2018/November/5be7eb6f_processed-celeba-small/processed-celeba-small.zip)) 
  which contains images of celebrities. The images in CelebA images has been cropped to remove parts of the image that don't 
  include a face, then resized down to 64x64x3 NumPy images. 
  
  Generative Adversarial Networks contains two networks.
  1. Generator: Generates fake images
  2. Discriminator: Detects if an image is real or fake
  
  These two models fight against each other and both of them develop at the same time. The generator tries to produce 
  images in such a way that discriminator should think those images are real. On the other hand, discriminator tries to 
  correctly identify the real images and the fake images produced by generator. Both the models are built using 
  Convolutional Neural Networks(Transpose convolutions in generator), BatchNorm layers and fully connected layers. 
  From reading the [Original DCGAN paper](https://arxiv.org/pdf/1511.06434.pdf), they say:
  > All weights were initialized from a zero-centered Normal distribution with standard deviation 0.02.
  
  Some of the hyper parameters chosen in the project are referred from the [Original DCGAN paper](https://arxiv.org/pdf/1511.06434.pdf) 
  like learning rate, beta1, beta2 for Adam optimizer and values for weight initialization and finally the model is trained on 
  the GPU. The input images and model produced images are shown below. For detailed description, refer the notebooks.
  
  #### Input
  ![Input images to model](https://github.com/Surya-Prakash-Reddy/Face-Generation/blob/master/assets/input.png "Input images to model")
  #### Output
  ![Output images from model](https://github.com/Surya-Prakash-Reddy/Face-Generation/blob/master/assets/output.png "Output images from model")
  

## Languages or Frameworks Used 

  * Python: language
  * NumPy: library for numerical calculations
  * Matplotlib: library for data visualisation
  * Pytorch: a deep learning framework by Facebook AI Research Team for building neural networks
  * torchvision: package consists of popular datasets, model architectures, and common image transformations for computer vision
  
## Setup
  
  To use this project, clone the repo
  
  ### Clone
  ```
    git clone https://github.com/Surya-Prakash-Reddy/Face-Generation.git
  ```
  
  After cloning, you can use the `dlnd_face_generation.ipynb` notebook to modify the notebook or generate realistic looking faces. If you want to learn how to generate images and replicate the notebook, you can use `dlnd_face_generation.html` file.
