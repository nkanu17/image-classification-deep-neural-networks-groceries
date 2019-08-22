# Introduction and Analysis of Problem

In this project, image classification is performed using three different types of deep convolutional neural networks in order to classify groceries of fruits, vegetables, and packaged liquid. The dataset was created based on the [Grocery Store Dataset](https://github.com/marcusklasson/GroceryStoreDataset) found on github, with images from 81 different classes of fruits, vegetables, and packaged products. See code for reference

For the purpose of this project, the dataset was re-classified into 3 classes of fruits, vegetables, and packages. It was reclassified into three different classes in order to learn how a neural network can be trained to differentiate on a higher level between fruits, vegetables, and packaged poducts each having numerous sub-types.
## 
This problem is applicable to create any future intelligent grocery store that can easily recognize differences in groceries. This may provide an insight into creation of stores where cash registers and cashiers may no longer be necessary - saving time, money, and resources for customers and businesses.

# CNN overview

Created a small convolutional network as baseline for analysis and then used VGG16 and ResNet50 for transfer learning.

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

Perform GridSearch or use Thalos for more thorough hyperparameter tuning. This is still to come.

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

The ResNet50 proved to be the best model in terms of both accuracy and loss. The accuracy validation results ranged around 98-99% while the confusion matrix described only one image (fruits) classified incorrectly. In conclusion, the problem of classifying different groceries at a high level can be solved using multiple convolutional neural networks such as the ResNet50. With a good, sufficient(large) dataset, this network can definitely be used in real life situations.

# Citation
@inproceedings{klasson2019hierarchical,
  title={A Hierarchical Grocery Store Image Dataset with Visual and Semantic Labels},
  author={Klasson, Marcus and Zhang, Cheng and Kjellstr{\"o}m, Hedvig},
  booktitle={IEEE Winter Conference on Applications of Computer Vision (WACV)},
  year={2019}
}
