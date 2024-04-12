# CNN-Architecture-VGG16-and-ResNet50
## Comparison of VGG16 and ResNet50 CNN Architectures for Facial Attribute Detection

### Dataset Preparation
The dataset for this project was provided by the Course Leader, based on my ID. After requesting additional data, the dataset was expanded to a total of 3,998 images, including both human and non-human subjects. The dataset identifies five facial attributes:

- **Wrinkles**: Classified as 0 (no wrinkles) or 1 (has wrinkles)
- **Freckles**: Classified as 0 (no freckles) or 1 (has freckles)
- **Glasses**:
  - 0: Does not wear glasses
  - 1: Wears normal glasses
  - 2: Wears sunglasses
- **Hair Color**: Eight classes ranging from brown to not visible
- **Hair Top**: Four classes, including bald/shaved and not visible

Initially, a Python script was used to convert the image files into video format (.mp4), which was subsequently converted to .mov using an online tool. The images were annotated using a specialized tool, generating 7,996 data frames. Duplicate images were excluded. The data was saved in a CSV file with columns for each attribute. Numpy arrays were used to handle the data, which was normalized (values between 0 and 1) and resized to 50x50 pixels for processing.

### Model Training and Testing
Both VGG16 and ResNet50 models were trained on the dataset. The data was split into training and testing subsets.

#### Model Accuracy
- **Wrinkles**: Both models achieved a validation accuracy of 0.82, with less overfitting observed in VGG16.
- **Freckles**: Both models achieved a validation accuracy of 0.99.
- **Glasses**: Both models reached a validation accuracy of 0.91, with ResNet50 showing more overfitting.
- **Hair Color**: Both models had a lower validation accuracy of 0.24.
- **Hair Top**: Both models achieved a validation accuracy of 0.61.

Overall, VGG16 outperformed ResNet50, particularly in terms of handling overfitting, which was less prevalent in the VGG16 model.

### Comparison
VGG16 is generally more effective for our dataset, likely due to the absence of residual blocks, which seems to suit our specific data characteristics better.

### Data Augmentation
To address the relatively small size of the dataset, data augmentation techniques such as horizontal flipping, rotation, and zoom were applied. This significantly helped in reducing overfitting.

### Testing Results
The testing phase showed high accuracy for attributes like wrinkles, freckles, and glasses, but the results for hair color were unsatisfactory due to the poor model performance on this attribute.

