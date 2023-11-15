# WCGAN-GP-Imagenes-Coloidales
The Wasserstein Conditional Generative Adversarial Network with Gradient Penalty, abbreviated as WCGAN-GP, is a model developed by  [Walia, Tierney and McKeever 2020](https://www.researchgate.net/publication/347437993_Synthesising_Tabular_Data_using_Wasserstein_Conditional_GANs_with_Gradient_Penalty_WCGAN-GP)   for data generation. The WCGAN-GP uses the Wasserstein loss along with the gradient penalty. This approach contributes to greater stability during training. In addition, it stands out for being a conditional GAN, which implies its ability to generate conditional data according to the input label.

In this repository you will find 3 scripts. The first is the WCGAN-GP and exemplifies its application by generating synthetic data from a specific data set (Images obtained through bright field video microscopy). It is worth noting that, in this context, WCGAN-GP has been adapted to generate statistically equivalent quasi-2D colloidal images. 
. The second is called tracking.py and is used to track particles. The last file graph_g(r) is used to calculate the radial distribution function (rdf) known as g(r). This is a metric that is used to compare the images generated by the WCGAN-GP and the experimental images.

## Run 
Take into account that the code was executed in Google Colab and the images with which it was trained are found on a drive.


## Load the Model
Once the model is trained we use the command “model.save_weights” it is a function that is used to save the weights of a neural network model in a file. Saving the model can help save the progress of a training model so that training can be resumed at a later date without having to start from scratch. To do this, you also need to save the discriminator and the generator. The “discriminator.save” command saves the discriminator architecture to a file. The “generator.save” command is used to save the generator architecture to a file. These commands can be useful for sharing models with other users or for using a trained model in different applications.
Once the file is saved, it can be loaded again using the “model.load$\_$weights” and “load$\_$model” commands. The first command loads the weights of a neural network model and the second command is used to load the generator and discriminator.
