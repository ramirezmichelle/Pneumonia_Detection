# Pneumonia_Detection
Fine-tune VGG16 CNN using Keras to detect and predict if chest xrays from NIH Kaggle Dataset are indicative of pneumonia. Dataset found here: https://www.kaggle.com/nih-chest-xrays/data

## Patient Demographic From Dataset ##

Our dataset consisted of male (63328) and female (48776) patients aged 1-95 years, with most patients falling in the range of 40-60 years old. Chest X-rays from both PA (Posterior Anterior) and AP (Anterior Posterior) views were taken.

### Co-Occuring Diseases ###
The following plot shows co-occuring diseases in x-rays that showed pneumonia was present in our dataset. It is important to understand if other diseases are present as they may affect the pixel-intensities of the chest x-ray taken.

<img src="images/EDA/co_occuring_diseases.png" width="500">

### Pixel-Level Assessments of Imaging Data ###
The following images show what cases where the patient is healthy (No disease findings in chest xrays) and cases where pneumonia is present in the chest xrays. Accompanying the xray figures is a series of pixel intensities. 

#### Healthy Data (no pneumonia or other conditions) ####
<img src="images/EDA/healthy_xrays.png" width="500"> <img src="images/EDA/healthy_xrays_intensities.png" width="500">

#### Pneumonia Chest-Xrays ####
<img src="images/EDA/pneumonia_xrays.png" width="500"> <img src="images/EDA/pneumonia_intensities.png" width="500">

## Dataset ##
Training Dataset - Split to contain 1145 positive cases (pneumonia present) and 1145 negative cases (no pneumonia). The dataset was split in a 50/50 manner to allow our model to train fairly on both situations. The training dataset also had image augmentations done (rescaling, height shift, width shift, rotation by a 20 degree angle, shear, zoom).

Validation Dataset - Split to contain 286 positive cases (pneumonia present) and 1144 negative cases (no pneumonia). The dataset was split in a 20/80 manner to give our model a more realistic set of data, where there is an imbalance in the cases of pneumonia.

## Model Architecture ##




## Evaluation Metrics ##
For our model, we decided to optimize for the maximum **F1 score** our model could produce. Because there are class imbalances between cases of pneumonia and no pneumonia, and our dataset is rather small, F1 score was chosen to measure the test's accuracy. 

F1 score combines both precision and recall for binary classification problems, taking into account the amount of **true positives**, **false negatives**, and **false positives**. F1 can be calculated as follows:
<img src= "images/F1_formula.png" width = 200>

F1 score is maximized when there is a balance between precision and recall.

### Precision ###

### Recall ###

### Threshold ###

### F1 Score ###


## 
