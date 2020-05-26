# Image Classification using CNN and Transfer Learning
The dogs vs cats dataset refers to a dataset used for a Kaggle machine learning competition held in 2013.

The dataset is comprised of photos of dogs and cats provided as a subset of photos from a much larger dataset of 3 million manually annotated photos. The dataset was developed as a partnership between Petfinder.com and Microsoft.
https://www.microsoft.com/en-us/research/publication/asirra-a-captcha-that-exploits-interest-aligned-manual-image-categorization/

# Problem Faced during project Implementation :
1. This dataset contains 25,000 label images, during pre-processing RAM used to crash every time load the dataset.
   which help me realize that the size is big for machines to handle. So I used TensorFlow flow_from_directory which 
   does not load all data into RAM, it takes the image directly from directory.
2. During importing VGG16 model requires changing of output label because initially it is developed for 10 class classification.

# Steps :
# 1. Importing and Unzipping Data from Drive
     I used google colab as my IDE to implement this project which requires data uploading on a regular basis. 
     To save time, I uploaded the dataset to drive and gave direct access to the dataset.
# 2. Pre-Processing Image data
     i)  Normalization :
         Image pixel value lies between the range of 0-255 to normalize, which requires to bring value between the range 
         of 0-1. we divide each pixel by 255.
     ii) Resize :
         An image dataset, it does not necessarily have an equal resolution. 
         We need to bring each image into an equal resolution.
    iii) Data annotation :
         Data annotation is used when training data is less but on the other hand, 
         I believe data annotation gives us a different type of data to train a model for robustness.
         Data annotation consists of image rotation, image shifting, mirror image, etc.
# 3. CNN Model
      In this project instead of making my own CNN architecture, I used transfer learning.
      I used a pre-build VGG16 model architecture. 
# 4. Result and Plots
      Using transfer learning on the VGG16 model, I achieved approx 93% accuracy.
      As plot we observe our leanining of model in Cat_vs_Dog_classification.ipynb.

 

