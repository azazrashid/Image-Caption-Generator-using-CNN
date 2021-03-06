# Image-Caption-Generator-using-CNN
This repository has code for implementing the image caption generator using CNN (Convolutional Neural Networks) and LSTM (Long short term memory). The image features will be extracted from Xception which is a CNN model trained on the imagenet dataset and then we feed the features into the LSTM model which will be responsible for generating the image captions.

**Dataset**

For the image caption generator, we will be using the Flickr_8K dataset. There are also other big datasets like Flickr_30K and MSCOCO dataset but it can take weeks just to train the network so we will be using a small Flickr8k dataset. The advantage of a huge dataset is that we can build better models.
Thanks to Jason Brownlee for providing a direct link to download the dataset (Size: 1GB).

[Flickr8k_Dataset](https://github.com/jbrownlee/Datasets/releases/download/Flickr8k/Flickr8k_Dataset.zip)
[Flickr8k_text](https://github.com/jbrownlee/Datasets/releases/download/Flickr8k/Flickr8k_text.zip)

The Flickr_8k_text folder contains file Flickr8k.token which is the main file of our dataset that contains image name and their respective captions separated by newline(“\n”).

**Required Libraries**

*tensorflow
*keras
*pillow
*numpy
*tqdm
*jupyterlab

**Training and Testing Model**
To train the model run the juyter notebook to load the data and generate the necessary files and the trained model. When the model has been trained, now, run the testing_caption_generator.py file which will load the model and generate predictions. The predictions contain the max length of index values so we will use the same tokenizer.p pickle file to get the words from their index values.  
