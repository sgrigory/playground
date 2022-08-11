# Turning image classifier into a image generator

Given a pre-trained image classification model, can we reconstruct the images corresponding to each class? Naively, one could achieve this by inverting the usual training process: instead of tuning the model weights given a fixed input image, we'll fix the model weights and tune the input image trying to maximize probability of one of the classes. If this works, this would allow to turn any image classification model into an image generator.

- `generative_mnist.ipynb` shows how this works on MNIST - reconstruction is far from ideal, but digits are (often) recognizable
- `imagenet_lightning_current.ipynb` is an attempt to do the same for EfficientNet pre-trained on ImageNet. That doesn't generate anything good yet