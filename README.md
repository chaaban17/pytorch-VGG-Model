# pytorch-VGG-Model

training a pretrained ImageNet VGG-19 model on CIFAR10:
adding data augmentation on the dataset,
using ADAM as the gradient optimizer
and adding L2 regularization 

the purpose of this repository is to use this trained model on a different dataset in the near future.

# Prerequisites

you should install torch, torchvision, matplotlib, Pillow, numpy
OR simply run the project in Google Colab: https://colab.research.google.com/ and import the packages

# TransferLearning

This model is a pretrained VGG1-19 ImageNet model. I froze the weights and trained the feature classifier layer; I also edited the output features since we have 10 classes in CIFAR-10.
Hyperprametes: Epochs: 10 (this is a bit low but took almost 2 hrs on Cuda) Batch size=128, Optimizer: SGD and Loss: Cross entropy loss. no L1 nor L2 losses were added.

# firstModel and SecondModel

These two models are also VGG-19 pretrained models. I increased the number of epochs to 15, used ADAM and flipped and rotated the CIFAR dataset.added weight decay for the 1st and removed it in the 2nd.

# Observations

I got decent results in the transfer learning (first trial) but they were not good enough.

the two new models were clearly underfit. I should increase the number of epochs.

Hopefully this can be done in the near future.

