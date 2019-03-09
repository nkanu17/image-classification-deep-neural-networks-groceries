# Introduction and Analysis of Problem

This project introduces the field of computer vision through image classification using deep convolutional neural networks to address the problem of recognizing and classifying different grocery products. Computer vision is a field of science and technology that extracts, processes, and analyzes information from digital images and videos in order to replicate human perception and gain a higher level understanding of the world. Image classification, a subject of pattern recognition in Computer Vision, finds different characteristics and relationships of image data by categorizing its pixels into the several classes. One possible field of application of the image detection is automatic groceries image recognition. 

In this project, image classification is performed using three different types of deep convolutional neural networks in order to classify groceries of fruits, vegetables, and packaged liquid. The dataset was created based on the [Grocery Store Dataset](https://github.com/marcusklasson/GroceryStoreDataset) found on github, with images from 81 different classes of fruits, vegetables, and packaged products.

For the purpose of this project, the dataset was re-classified into 3 classes of fruits, vegetables, and packages. It was reclassified into three different classes in order to really see if a neural network can be trained to differentiate on a higher level between fruits, vegetables, and packaged poducts each having numerous sub-types. For instance, there are different types of fruits such as apples, bananas, avacados, and kiwis, each with different shape and texture. Similarly, there are different vegetables such as tomatoes, potatoes, etc. The network can easily differentiate between bananas and tomatoes, but can it really differentiate between a tomato and an apple between all the other sub-types? What about confusing the texture of a kiwi to that of a potato, or an avocado for a vegetable? This problem is applicable to create any future intelligent grocery store that can easily recognize differences in groceries. This may provide an insight into creation of stores where cash registers and cashiers may no longer be necessary -saving time, money, and resources for customers and businesses.

# Dataset

**Source**

The images of this dataset is found on another dataset, [Grocery Store Dataset](https://github.com/marcusklasson/GroceryStoreDataset), of natural grocery items found in Github. It was transformed to fit the goals of this project.

Classes: 


1.   Fruits
 - Train set: 500 images
 - Validation set: 100 images
 - Test set: 100 images

2.   Packages
 - Train set: 500 images
 - Validation set: 62 images
 - Test set: 100 images

3.   Vegetables
 - Train set: 500 images
 - Validation set: 100 images
 - Test set: 100 images

Types of Fruits in data set: 

 - Apple, Avocado, Banana, Kiwi, Lemon, Lime, Mango, Canteloupe, Galia-Melon, Nectarine, Orange, Papaya, Passion-Fruit, Peach, Kaiser, Pineapple, Plum, Pomegranite, Red-Grapefruit, Satsumas, Watermelon, Honeydew Melon, Anjou, Conference


Types of Vegetables in data set:
 - Asparagus, Aubergine, Cabbage, Carrots, Cucumber, Garlic, Ginger, Leek, Mushroom, Onion, Pepper, Potato, Red Beet, Tomato, Zucchini
 
Types of Packages in data set:
- Juice, Milk, Outghurt, Oat-Milk, Sour-Cream, Sour-Milk, Soyghurt, Soy-Milk, Yogurt

# Future optimizations

Goal is to perform GridSearch or use Thalos for more thorough hyperparameter tuning. This is still to come.

# Final Results

When comparing the following accuracy of all the models:

1.   Baseline Convolution Model with dropout layer
 - validation accuracy around 86%, 35/262 images classified incorrectly
2.   VGG16 transfer model with dropout layer
 - validation accuracy range of 86-89%, 26/262 images classified incorrectly
3.   VGG16 transfer model without dropout layer
 - validation accuracy range of 89-90%, 18/262 images classified incorrectly
4.   VGG16 transfer model with learning rate changed from 1e-4 to 1e-5
 - validation accuracy range of 92-94%, 17/262 images classified incorrectly
5.   ResNet50 transfer model
 - validation accuracy around 99%, only 1/262 images classified incorrectly

The ResNet50 proved to be the best model in terms of both accuracy and loss. The accuracy validation results ranged around 98-99% while the confusion matrix described only one image (fruits) classified incorrectly. In conclusion, the problem of classifying different groceries at a high level can be solved using multiple convolutional neural networks such as the ResNet50. With a good, sufficient(large) dataset, this network can definitely be used in real life situations, the same cannot be said for the VGG models because the accuracy rates and predictons were not good enough.

