# Melonoma_CNN_Assignment
> Building a CNN based model which can accurately detect melanoma. Melanoma is a type of cancer that can be deadly if not detected early. It accounts for 75% of skin cancer deaths. A solution that can evaluate images and alert dermatologists about the presence of melanoma has the potential to reduce a lot of manual effort needed in diagnosis.


## Table of Contents
* Melanoma-Detection-using-using-custom-cnn
Table of Contents
* General Information
	- Dataset Information
	- Steps Involved
	- Results
	- Baseline Model
	- Augmented Model
	- Final Model
* [Technologies Used](#technologies-used)
* [Conclusions](#conclusions)
* [Acknowledgements](#acknowledgements)

## General Information
- Problem statement: To build a CNN based model which can accurately detect melanoma. Melanoma is a type of cancer that can be deadly if not detected early. It accounts for 75% of skin cancer deaths. A solution that can evaluate images and alert dermatologists about the presence of melanoma has the potential to reduce a lot of manual effort needed in diagnosis.
  - The dataset consists of 2357 images of malignant and benign oncological diseases, which were formed from the International Skin Imaging Collaboration (ISIC). All images were sorted according to the classification taken with ISIC, and all subsets were divided into the same number of images, with the exception of melanomas and moles, whose images are slightly dominant.


The data set contains the following diseases:

	- Actinic keratosis
	- Basal cell carcinoma
	- Dermatofibroma
	- Melanoma
	- Nevus
	- Pigmented benign keratosis
	- Seborrheic keratosis
	- Squamous cell carcinoma
	- Vascular lesion


#### Project Pipeline
- Data Reading/Data Understanding → Defining the path for train and test images 
- Dataset Creation→ Create train & validation dataset from the train directory with a batch size of 32. Also, make sure you resize your images to 180*180.
- Dataset visualisation → Create a code to visualize one instance of all the nine classes present in the dataset 
- Model Building & training : 
    Create a CNN model, which can accurately detect 9 classes present in the dataset. While building the model rescale images to normalize pixel values between (0,1).
- Choose an appropriate optimiser and loss function for model training
- Train the model for ~20 epochs
- Write your findings after the model fit, see if there is evidence of model overfit or underfit
- Choose an appropriate data augmentation strategy to resolve underfitting/overfitting 
**Model Building & training on the augmented data :**
  - Create a CNN model, which can accurately detect 9 classes present in the dataset. While building the model rescale images to normalize pixel values between (0,1).
  - Choose an appropriate optimiser and loss function for model training
  - Train the model for ~20 epochs
  - Write your findings after the model fit, see if the earlier issue is resolved or not?
**Class distribution: **
  - Examine the current class distribution in the training dataset 
  - Which class has the least number of samples?
  - Which classes dominate the data in terms of the proportionate number of samples?
**Handling class imbalances:** 
  - Rectify class imbalances present in the training dataset with Augmentor library.
**Model Building & training on the rectified class imbalance data:**
  - Create a CNN model, which can accurately detect 9 classes present in the dataset. While building the model rescale images to normalize pixel values between (0,1).
  - Choose an appropriate optimiser and loss function for model training
  - Train the model for ~30 epochs
  - Write your findings after the model fit, see if the issues are resolved or not?
  - 

## Conclusions
- Conclusion 1 from the analysis
	Too early to say overfitting or underfitting, Validation accuray and Training accuracy follow each other.
	Training loss is low but validation loss is fluctuating
- Conclusion 2 from the analysis
  	The accuracy remains the same as per first. But still low accuracy
	- Which class has the least number of samples?
		-- seborrheic Keratosis
	- Which classes dominate the data in terms proportionate number of samples?
		-- Melanoma and Pigmented benign keratosis actinic keratosis and dermatofibroma
  
- Conclusion 3 from the analysis

 Now we have added 500 images to all the classes to maintain some class balance. 
- pigmented benign keratosis    962
- melanoma                      938
- basal cell carcinoma          876
- nevus                         857
- squamous cell carcinoma       681
- vascular lesion               639
- actinic keratosis             614
- dermatofibroma                595
- seborrheic keratosis          577

![image](https://github.com/gowdaKM/Melanoma_CNN_Assignment/assets/131829909/d08c2aac-2174-4d33-87d3-d4b8afad778f)

- Validation accuracy is around .889
- Training and validation accuracy follow eachother
- Same with Training and Validation loss.


## Technologies Used
- tensorflow
- matplotlib
- numpy
- pandas
- PIL

