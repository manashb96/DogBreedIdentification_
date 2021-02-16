# DogBreedIdentification_

According to the data provided from Kaggle the format was such that we had 2 folders of test and train along with the labels csv file with names from the train directory and a sample_submission file with the names of the test directory.  

To access train data we created a function to add pixel values of a photo by using `load_img` to convert an image into PIL format and then converting them to numpy array using img_to_array and loading the labels using a dictionary to map it with the unique dog breeds  

Now we get the feature maps using Transfer Learning via InceptionV3 network and ResNet101 network.  
We concatenate these features into one and then create a separate head model with a Dense layer to give us the final results.  
We fit the head model on the concatenated feature maps extracted from the two networks.  
We then plot a 3x2 figure with title as predicted dog breed and the percentage as predicted probabilities.  
