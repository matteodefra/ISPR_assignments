# Midterm 3

[Midterm 3](assignment3/) consisted in the implementation of a Denoising AutoEncoder trained over the [MNIST](http://yann.lecun.com/exdb/mnist/) dataset.

The autoencoder was implemented by first layerwise pretraining of the single hidden layer, then the pretrained layers were put together to build a Deep AutoEncoder. 
The resulting Deep AutoEncoder was used with and without finetuning, collecting the results over the training and testing set of the dataset.

On final finetuned Deep AutoEncoder was performed a latent space interpolation, by using the hidden representation of the images, and the gradient ascent process resulting from the Manifold learning of the Denoising AutoEncoder.
