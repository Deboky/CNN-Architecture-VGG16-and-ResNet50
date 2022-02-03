# CNN-Architecture-VGG16-and-ResNet50
Comparison of two CNN architecture VGG16 and ResNet50 for detecting Facial attribute
**DATASET PREPARATION**
 Image data has been provided by the Course Leader based 
on my ID - 001142694, and after requesting an extra dataset, 
the total dataset consisted of 3998 images. The data 
comprises both human and not human images. There are five 
attributes considered: wrinkles, freckles, glasses, hair color, 
and hair top. Wrinkles have two classes which are 0 and 1 
where 0 means does not have wrinkles, and 1 means it has 
wrinkles. Similarly, Freckles have two classes which are 0 
and 1 where 0 means does not have freckles, and 1 means it 
has freckles. Glasses has three classes where 0 refers to ‘Does 
not wear glass’, 1 refers to ‘Wear Normal Glass’ and 2 refers 
to ‘Wear Sunglasses’. Next, the hair color has 8 classes where 
0 means ‘Brown’, 1 denotes ‘Black’, 2 indicates ‘Gray’, 3 
represents ‘Blond’, 4 implies ‘Red’, 5 means ‘White’, 6 
denotes ‘Mixed’, 7 means ‘Others’ and 8 implies ‘Not 
visible’. Lastly, hair color has 4 different classes where 0 
refers to ‘Bald or shaved’, 1 indicates ‘has few hairs’, 2 refers 
‘has thick hair’ and 4 represents ‘Not visible’. Initially, a 
python script was provided to convert the images into video 
(.mp4). An online converter has been used to convert .mp4 
file to .mov. After that, an annotation tool has been used to 
label the attributes, and after the completion of 7996 data 
frames, a text file was generated. The duplicate images have 
been skipped. The text file was then converted into .csv file 
where the first column indicates the image names and the 
second column has the labels of wrinkles, the third has the 
labels of freckles, fourth has the labels of glasses, fifth the 
labels of hair color, and lastly, the sixth column has the labels 
of hair top. Then, five numpy arrays have been created to 
convert the feature data, which is further used for training. It 
is then normalized by dividing it by 255 so that the values 
range between 0 and 1. The image has been resized, and it is 
taken as 50 by 50. The data has been split into training and 
testing, and then it is feed to the network.

The model accuracy using both VGG16 and Resnet50 has
been compared and the best models have been chosen to 
perform the testing.

**A. Model Accuracy with VGG16 and Resnet50 for attribute 
wrinkles**
 After training the model with 10 epochs, the accuracy 
received is shown in the graph below. For wrinkles, both 
VGG16 and Resnet50 give a validation accuracy of 0.82. 
However, overfitting is observed more on the Resnet50. 
Overfitting occurs when a model learns a function with high 
variance to model the training data accurately. 

**B. Model Accuracy with VGG16 and Resnet50 for attribute 
freckles**
The validation accuracy for freckles in both the models give 
the same result and it is 0.99.

**C. Model Accuracy with VGG16 and Resnet50 for attribute 
Glasses**
 The validation accuracy for glasses in both the models give 
the same result and it is 0.91. However, there is more 
overfitting in the Resnet50

**D. Model Accuracy with VGG16 and Resnet50 for attribute 
Hair color**
The validation accuracy with hair color is poor and it is 0.24 
in both the cases

**E. Model Accuracy with VGG16 and Resnet50 for attribute 
Hair top**
The validation accuracy with VGG16 and Resnet50 are 
same in both the cases and it is 0.61.

**Comparison between VGG16 and Resnet50**
 In the given dataset, VGG16 gives better performance than 
Resnet50 as the overfitting problem is found less in the 
VGG16 model which is why it is used for testing. One of the 
reasons of better performance in VGG16 could be because it 
has no residual block. Moreover, the given dataset is well 
suited to VGG16.

**Data Augmentation**
The dataset given contains 3998 images which is not huge 
and thus data augmentation solves the problem. Data 
augmentation refers to a collection of techniques that expands 
the size and quality of training dataset to develop deep 
learning models. In the implementation, horizontal flip, 
rotation, and zoom has been executed. After data 
augmentation, the overfitting has been reduced to a great 
extent.

**Testing Results**
 It is visible from the figures below that the prediction 
results for wrinkles, freckles, hair top and glasses are nearly 
accurate. However, the prediction with the hair color is not 
satisfactory. It is because the accuracy rate of hair color is 
poor
