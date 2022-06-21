# Braille-to-Text-Translator
This repository is meant to store our Final Project for the Image processing class (SSC0251) in the USP University on ICMC.

Members of the group:

Luca Gomes Urssi - 10425396

Alecxannder Jellicoe Sonnenberg Brizotto Ferreira - 10295707

- Main objective:
  
  Our project has as it's goal to translate braille into text. We will start aiming to achieve 1 letter in braile : 1 letter in the alphabet + some special
  symbols. Once this is done we may try to apply it to a sentence/text.
  
- Input Images:
  
  The input for our program will be images of braille characters, which will be sourced from datasets and searched manualy by the group members.
  
  - Image Source: https://www.kaggle.com/datasets/shanks0465/braille-character-dataset?resource=download, these images contain braile letters in varying conditions
  of light,noise and quality.
  
    Examples:
  
    ![a1 JPG3whs](https://user-images.githubusercontent.com/26423265/174901385-4478861c-5f01-40ab-8e11-1cf0bf063ad4.jpg) ![a1 JPG0dim](https://user-images.githubusercontent.com/26423265/174901162-e322476a-7810-4279-9ecc-7f4a3c91e90c.jpg) ![a1 JPG2dim](https://user-images.githubusercontent.com/26423265/174901275-89d16570-cce4-4c5e-b7fb-7818c00900e3.jpg)
![b1 JPG11whs](https://user-images.githubusercontent.com/26423265/174901564-372cd178-07f0-400d-946a-5e9d04866ff8.jpg) ![b1 JPG3dim](https://user-images.githubusercontent.com/26423265/174901513-08f6cdae-46e3-4664-8723-565ae89f4620.jpg) ![b1 JPG0dim](https://user-images.githubusercontent.com/26423265/174901502-66981c79-a034-4d0f-9532-b4942ff36f88.jpg)


  - Manually Searched/Made: Some of the images were made by us (none of these), they are mostly for testing.
  
    Examples:
  
    ![M](https://user-images.githubusercontent.com/26423265/174901217-928458a1-6de4-4b66-9a81-2339a8444c5f.png) ![L](https://user-images.githubusercontent.com/26423265/174901758-3f8e5bc9-456d-4f5f-96f8-080597b45438.png) ![E](https://user-images.githubusercontent.com/26423265/174901769-6a7b3bce-1537-4af2-b940-7c06243eb369.png) ![A](https://user-images.githubusercontent.com/26423265/174901776-28a44f47-ad42-4053-ab6a-1c0315b08c92.png)

  
- Image processing steps:
  - Pre-processing:
  
    For this step we took the input image (from the dataset above) and used Luminance to turn it into grayscale, normalized this image so if it was
    too dark, black pixels wouldn't affect the next process, the binarization, using a threshold T to make the regions that have any braile balls get white
    and the space in between them black. As the final process we are planning to use k-means clusterization to detect 0-6 clusters which will give us the 
    center of mass of the circles and that will be used to plot more realistic circles instead of "random stains". To find K we are dividing the image in 6 sextants
    and detecting wheter or not the sum bigger than 0. This method has several flaws such as not being effective if there is any rotation/translation in the image
    but works for the proof of concept phase of the assignment. We may try to fix it.
    
  - Processing:
  
    Once we have more adequate images we will compare, with euclidian distance, them with the ones in our dictionary (made manually by us) and output the respective  '   letter. With this is done we may start working on how to apply it to a full sentence/text by methods we are still to figure out.
    
  - What we are thinking we could possibly use:
    Morphology could prove a better way to approach the problem of finding K in those tricky cases, maybe via blob detection.
    We are going to use K-means to calculate the approximate centroid of the braile blobs, then use them to plot a new image, with better looking circles.
    We will use Euclidian distance or similarity to compare them to images we have acquired that are going to work as a dictionary.
    For sentences and texts we may need to use a CNN or something like that and we don't have any idea how to do this.
   
    
    
