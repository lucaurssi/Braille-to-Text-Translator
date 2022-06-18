# Braille-to-Text-Translator
This repository is meant to store our Final Project for the Image processing class (SSC0251) in the USP University on ICMC.

Members of the group:

Luca Gomes Urssi - 10425396

Alecxannder Jellicoe Sonnenberg Brizotto Ferreira - 10295707

- Main objective:
  
  Our project has as it's goal to translate braille into text. We will start aiming to achieve 1 letter in braile: 1 letter in the alphabet + some special
  symbols. Once this is done we may try to apply it to a sentence/text.
  
- Input Images:
  
  The input for our program will be images of braille characters, which will be sourced from datasets and searched manualy by the group members.
  Image Source: https://www.kaggle.com/datasets/shanks0465/braille-character-dataset?resource=download
  
- Image processing steps:
  - Pre-processing:
    For this step we took the input image (from the dataset above) and used Luminance do turn it into grayscale, normalized this image so if it was
    too dark black pixels wouldn't affect the next process, the binarization, using a threshold T to make the regions that have any braile balls get black
    and the space in between them white. As the final process we are planning to use k-means clusterization to detect 0-6 clusters which will give us the 
    center of mass of the circles and that will be used to plot more realistic circles instead of "random stains".
    
  - Processing
    Once we have more adequate images we will compare, with euclidian distance, them with the ones in our dictionary (made manually by us) and output the respective letter. Once this is done we may start working on how to apply it to a full sentence/text
    
    
