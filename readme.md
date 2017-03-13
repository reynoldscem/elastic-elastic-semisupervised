# Elastic Elastic Semi-Supervised

Sometimes I like to make strange models out of curiosity.

This is a classifier based on the following:

An shallow autoencoder with dropout and elasticnet regularisation is trained on MNIST with elastic distortions.

Codes from the hidden layer are then transformed into distance space for a minibatch KMeans model on the (labelled) val set.

These distance vectors are then used to train an SVM with an RBF kernel.

Achieves about 94% accuracy on the test set with a final feature size of about 100, having seen labels for only 10k examples.

I imagine far fewer labels would be viable too.
