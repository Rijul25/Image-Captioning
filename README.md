# Image-Captioning
Image captioning on Flickr dataset using CNN and LSTM

# This project gives us captions of an image.

### You can download the dataset from the following link-
https://www.kaggle.com/hsankesara/flickr-image-dataset

### This file contains 2 Files-
1.Flicker8k_Dataset ---> which contains images
2.Flickr8k_text ----> which contains text file such as .->
2.1 token.txt
2.2 train_images.txt
2.3 test_images.txt

## So this is what I did in Every notebook.
## Data_split.py ---->
### In this notebook I loaded the dataset and split it into 3 parts namely-
X_train, X_val, X_test

## Text and image_pre.py ---->
In this notebook I preprocessed the data and tokenized the sentences. I also used word2indices and indices2words vectorization so that we would get a caption in the form of -->
<start> caption <end>
  This makes our work easier and we make padded sequences which are like this <start> caption <end> only. In padded sequences One word is printed at a time and it goes on until the last word or the maximum length of sentences.
  Then I generated captions and next words and stored them as separate .npy files.
  Then I found out the no of images and image_names and their shape.
  
## Image embedding.py ->>>>
In this I devloped an embedding of each images using the resnet50 model and also calculated the train data which is a dicationary containing each image and its vector representation.

## image_cap.py--->
In this notebook I used 2 models- langauge and sequential and concatenated them to form one model using both CNN and LSTM cells.
At Last I gave the predictions and generated the caption using ArgmaxSearch which gives us the maximum value of the image array and generates the caption.

.............................................
