# Project: **Traffic signs classification and semantic segmentation using deep learning** 
**In this project, we used Python and TensorFlow to classify and recognize traffic signs.**

**Dataset used: 
For classification [German Traffic Sign Dataset](http://benchmark.ini.rub.de/?section=gtsrb&subsection=dataset).
This dataset has more than 50,000 images of 43 classes.**

For segmentation [Cityscapes Dataset](https://www.cityscapes-dataset.com/).



## Pipeline architecture:

1.   **Segmentation:**

- **Load The Data.**
    
- **Model Architecture.**
    - DeepLab.
    
- **Model Training and Evaluation.**

- **Testing the Model Using the Test Set.**

- **Extract the signs traffic objects.**



2.   **Classification**

- **Load The Data.**

- **Data Preprocessing**.
    - Resizing.
    - Cropping.
    
- **Design a Model Architecture.**
    - Resnet50
- **Model Training and Evaluation.**

- **Testing the Model Using the Test Set.**


We'll explain each step in details below.

#### Environement:
-  Ubuntu 19.10
-  Anaconda 5.3
-  Python 3.6
-  TensorFlow 1.12.0 (GPU support)
-  Spyder


---
## Step 1.1: Load The Data(semantic segmentation)

We downloaded dataset and convert to TFRecord.

There is  script (under the folder datasets) to convert Cityscapes dataset to TFRecord. First download the dataset beforehand by registering in the [website](https://www.cityscapes-dataset.com/).


---

## Step 3.1:  Model Architecture



### 1.Deeplab
DeepLab is a state-of-art deep learning model for semantic image segmentation,
where the goal is to assign semantic labels to every pixel in the input image.

---

## Step 4.1: Model Training 



---

## Step 5.1: Testing the Model using the Test Set

Now, we'll use the testing set to measure the accuracy of the model over unknown examples.

## Sample of the Result

![unnamed](https://user-images.githubusercontent.com/65299336/110251153-81c9eb00-7f7f-11eb-8f73-7f6c347b4b9e.png)


---

##  Step 6.1: Extract the signs traffic objects.

find the contours and draw a rectangular boundary to extract them.


## Step 1.2: Load The Data(classification)

Dataset Requirements
Dataset Folder should only have folders of each class. Dataloader will automatically split the dataset into training and validation data in 80:20 ratio.  
**Example:**

    .
    └── DatasetFolder
        ├── ClassOne                 
        │   ├── FirstImage.jpg                       
        │   ├── SecondImage.jpg                 
        │   └── ...    
        ├── ClassTwo  
        │   └── ...    
        ├── ClassThree               
        │   └── ...    
        └── ...

      

---

## Step 3.2: Data Preprocessing

In this step, we will apply several preprocessing steps to the input images to achieve the best possible results.

**We will use the following preprocessing techniques:**
1. Resizing.
2. Cropping.


---

## Step 3.2: Design a Model Architecture(classification)

In this step, we will use a deep learning model that learns to recognize traffic signs from our dataset [German Traffic Sign Dataset](http://benchmark.ini.rub.de/?section=gtsrb&subsection=dataset).

We'll use ResNet-50 that described in the paper "Deep Residual Learning for Image Recognition" (http://arxiv.org/abs/1512.03385). to classify the images in this dataset. 





---

## Step 4.2: Model Training and Evaluation

In this step, we will train our model using `normalized_images`, then we'll compute softmax cross entropy between `logits` and `labels` to measure the model's error probability.

---

## Step 5.2: Testing the Model using the Test Set

Now, we'll use the testing set to measure the accuracy of the model over unknown examples.

---

## Conclusion

To sum up our project has two steps, first we have the image of the street which has a lot of objects beside the traffic signs so we used the semantic segmentation to identify all objects in the image then we extracted only the traffic signs.After that, the second step job is to classify the extracted traffic signs to 43 classes we trained the model on but we faced a problem because some of extracted signs are not in 43 classes we have so we added

