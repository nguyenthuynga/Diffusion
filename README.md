# Score-Based Generative Modeling: Application for Space-Time Interpolation for Sea Surface Turbidity Reconstruction
This tutorial introduces a 3D input setting (2D spatial dimensions + 1D time series) using Unet3D with convolutional 3D layers.

The objective of this code is to perform interpolation (or fill gaps or conduct image inpainting) for sea surface turbidity datasets obtained through remote sensing as example below: 


![ncsnv2](https://github.com/nguyenthuynga/Diffusion/blob/main/Images/diffusion_generative.png?raw=true)
(The left is the gappy input that we want to do interpolation, the right is the ground truth. The three middle ones are three samples of the generative models)

You can access the code, download the data, and read more about the case study in the notebook main.ipynb above or the code +output results [here](https://drive.google.com/file/d/1GtDtlIpXjg5UvwvAl8sK1ZqtG9q5L3AY/view?usp=sharing). Notes that, to run faster, we run for small UNet, small number of epochs, and small samples. By increasing number of training epochs (n_epochs to 1000), increasing number of steps in sampling method (num_steps to 1000), and increasing the number of samples (N_experiments to 10 or more for examples), and increase the channels of UNet to [64, 128, 256, 512], we'll get a better interpolation, however it will increase the computing time a lot.

To understand more about the context of our case study, you can access [This slides](https://drive.google.com/file/d/1LToT3CvvatP-C9O1pP0Dl5LRoIT3NFbZ/view?usp=sharing) and [this article](https://drive.google.com/file/d/1ua0MAdwUuBBWKQ1M9NRoxbwqvJSqX1ID/view?usp=drive_link) . A comparison of hyperparameters can be found [here](https://docs.google.com/presentation/d/1d3EgBYWsMaPBOll0PB5HIhyn4hLQZnOwufLpnyQHsNc/edit?usp=sharing) .

If you have any questions or need clarification on any aspect of the code, please don't hesitate to contact me at nga.nguyen@imt-atlantique.fr.

### Acknowledgements

This tutorial is based on the methods of [This paper](https://arxiv.org/pdf/2011.13456.pdf) available at [Original Code for MNIST dataset with 2D setting and unconditiona generative model](https://colab.research.google.com/drive/120kYYBOVa1i0TD85RjlEkFjaWDxSFUx3?usp=sharing#scrollTo=XCR6m0HjWGVV).



