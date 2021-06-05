# Auto-Colorization of Grayscale Images using Generative Adversarial Networks (GANs)

### B.Tech Final Year Project

------------

First of all, upload the `Grayscale_Colorize.ipynb` file, `Convert_Grayscale.ipynb` file and `Grayscale_Colorize` folder to Google Drive exactly under the My Drive.

The model has been trained on a subset (50,000 images) of the Places 365 dataset. The dimension of images used for training is 256 x 256. The original Places 365 dataset contains 1.8 million images.

#### Steps to run using the Pre-Trained model

------------

Inside the folder, the file `G_Final.pth` is the finally trained generator which will be used.

Open `Grayscale_Colorize.ipynb` in Google Colab.

Change the runtime type to **GPU** and Mount Google drive.

Code cells that you need to run -> 1, 2, 3, 12, 13, 14, 15 and 16

In code cell 13, make sure that all file paths are valid.

Place your black and white images in the `Grayscale_Colorize/test_input` folder.

And after successful execution, the coloured images would be in `Grayscale_Colorize/test_output` folder.

You can use the `Convert_Grayscale.ipynb` script to convert images to grayscale.

#### Steps to train your own model

------------

Place your 256 x 256 training images from Places 365 or some other dataset **directly** under the `Grayscale_Colorize/places365` folder. Images should be renamed as `0.jpg`, `1.jpg`, `2.jpg` and so on.

Open `Grayscale_Colorize.ipynb` in Google Colab. Change the runtime type to **GPU** and Mount Google drive.

All the parameters and file paths are in Code cell 5

Run from top to bottom.

After the training is complete, go to `Grayscale_Colorize/checkpoints/weights` folder. The discriminator and generator associated with your last epoch are the final models. Only generator is needed to colorize new samples.
