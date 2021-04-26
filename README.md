# CNN From Scratch Attempt

This repo is two Jupyter Notebooks displaying my journey through attempting to implement a Convolutional Neural Network, without using a statistical learning library. 

I am aware I chose the two most vanilla CNN datasets I could possibly use, but having never built a CNN from scratch, these are good benchmarks. 

Start with [cifar_cnn.ipynb](https://github.com/kambielawski/cnn_from_scratch/blob/master/cnn_cifar.ipynb). This is where I spent most of my time struggling to make this thing work.

To summarize, I spent quite a lot of time watching ~5 videos in this series: [https://www.youtube.com/watch?v=l16RxAmP9QE](https://www.youtube.com/watch?v=l16RxAmP9QE). Video 52 went through all of the forward and backward propagation mathematics, which I used to implement. I spent a couple days banging my head against a wall on the CIFAR dataset - I was getting vanishing gradients and couldn't tell why. I switched to a 1-dimensional dataset (MNIST) to see if reducing complexity would help. It worked, but I found out that I had changed almost nothing in my code to make it work - the input *came* normalized, and after close inspection and debugging, I found out that was my problem with the CIFAR dataset. 

Anyway, if I hadn't lost all that time stagnating, I would've tried to expand the CNN to include more things. Like multiple ConvLayers, multiple fully-connected layers. I had this idea (I'm sure it's been tried) of doing dropout with a conv net, using one ConvLayer, many many filters, but dropping some filters at each forward propagation (or batch) to ensure we don't rely too heavily on a single filter and we see more diverse features from them.

