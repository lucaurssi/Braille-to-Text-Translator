# Braille-to-Text-Translator
This repository is meant to store our Final Project for the Image processing class (SSC0251) in the USP University on ICMC.

Members of the group:

Luca Gomes Urssi - 10425396

Alecxannder Jellicoe Sonnenberg Brizotto Ferreira - 10295707

- Main objective:
  
  Our project has as it's goal to translate braille into text and then text to bralle. Currently our project can receive an input image with 1 or more letters of braile and process it in a letter, word or phrase of text, it can also create a bralle text image out of text input. 
  
- Input Images:
  
  The input for our program will be images of braille characters, which will be sourced from datasets and searched manualy by the group members.
  
  - Image Source: https://www.kaggle.com/datasets/shanks0465/braille-character-dataset?resource=download, these images contain braile letters in varying conditions
  of light,noise and quality.
  
    Examples:
  
    ![a1 JPG3whs](https://user-images.githubusercontent.com/26423265/174901385-4478861c-5f01-40ab-8e11-1cf0bf063ad4.jpg) ![a1 JPG0dim](https://user-images.githubusercontent.com/26423265/174901162-e322476a-7810-4279-9ecc-7f4a3c91e90c.jpg) ![a1 JPG2dim](https://user-images.githubusercontent.com/26423265/174901275-89d16570-cce4-4c5e-b7fb-7818c00900e3.jpg)
![b1 JPG11whs](https://user-images.githubusercontent.com/26423265/174901564-372cd178-07f0-400d-946a-5e9d04866ff8.jpg) ![b1 JPG3dim](https://user-images.githubusercontent.com/26423265/174901513-08f6cdae-46e3-4664-8723-565ae89f4620.jpg) ![b1 JPG0dim](https://user-images.githubusercontent.com/26423265/174901502-66981c79-a034-4d0f-9532-b4942ff36f88.jpg)


- Image processing steps:
  - Pre-processing:
  
    For this step we took the input image (from the dataset above) and used Luminance to turn it into grayscale, normalized this image so if it was too dark, black pixels wouldn't affect the next process, the binarization, using a threshold T to make the regions that have any braile balls get white and the space in between them black.
    
  - Processing:
   
    As the final process we discretize the image, making it into a 2x3 matrix with binary values indicating if there is a dot on the location or not. With the processed matrix we can compare it with a dictionary of known combinations (bralle letters) and return the letter corresponding to the source bralle image.
    
 - Text-to-Bralle:
    
    Comparing the letter to the previous dictionary to find which bralle letter use and printing it to the output, appending images to or words or phrases.
