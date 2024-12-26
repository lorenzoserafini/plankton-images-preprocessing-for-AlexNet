# Plankton-images-preprocessing-for-AlexNet
Here we introduce a new image preprocessing technique specifically designed for classifying plankton images with AlexNet 3.

This approach allows the network to reach an accuracy of 85% on the given dataset.

- *Dai et al.*’s pre-processing method is not effective using AlexNet architecture.
- The *Unsharp* method, while not providing a significant improvement in accuracy, is the best pre-processing method among the ones tested.
- Applying *padding* before resizing the images has a positive effect on the accuracy of the net, increasing it by about 2%.

## Files
- The `Datas_44.mat` file contains the Dataset used to train and evaluate the model.
ZooScan is a dataset of 3771 images collected from the Bay of Villefranche-sur-mer using theZooscanteconlogy (G. Gorsky, M.D. Ohman, M. Picheral, S. Gasparini, L. Stemmann, J.B. Romagnan, et al., Digitalzooplankton image analysis using the ZooScan integrated system, J. Plankton Res. 32 (2010) 285–303. doi:10.1093/plankt/fbp124)
- The `make_square.m` file contains the function that pads the image in order to make it square.
- The `live_Net.mlx` file contains the program that trains and evaluate the model and saves the final confusion matrix.
	The rows between `%{` and `%}` contains the preprocessing method used in the paper 'A Hybrid Convolutional Neural Network for Plankton Classification' - Jialun Dai et al., in order to compare it with our method.
