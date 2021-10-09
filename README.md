
## DATA DESCRIPTION 
### 1. Samples
.jpg 10.239 mammographic images

.csv 6 files

### 2. Properties
The dataset contains:

753 calcification cases

891 mass cases

Density category

Breast: Left or Right

View: CC (craniocaudal) or MLO (mediolateral oblique)

The DDSM is a database of 2,620 scanned film mammography studies

### 3. Classes
It contains: normal, benign, and malignant cases with verified pathology information.

Pathology: Benign, Benign without call-back, or Malignant
![Flow chart of CBIS-DDSM preparation](https://github.com/ThyLy02/CBIS-DDSM-DATASET/blob/main/image/image1.png)


## LITERATURE REVIEW
### Methods
1. Image processing

Clip optical density values to be between 0.05 and 3.0 for noise reduction.

2. Image cropping

Abnormalities were cropped by determining the bounding rectangle of the abnormality with respect to its ROI.

3. Standardized train/test splits

The data were split into a training set and a testing set based on the BI-RADS (Breast imaging reporting and data system) category

20% of the cases for testing

80% of the cases for training

![Abnormalities in the Training and Test Sets](https://github.com/ThyLy02/CBIS-DDSM-DATASET/blob/main/image/image2.png)

### Performance evaluation

2 metrics: Accuracy & AUC (area under ROC curve)

![Flow chart of modeling process](https://github.com/ThyLy02/CBIS-DDSM-DATASET/blob/main/image/image3.png)

### Architecture
The texture analysis has been done on the region of interest (ROI) selected from the original mammogram

Using Support Vector Machine (SVM) classifier.

Pre-train: ImageNet/ InceptionV3 / ResNet-50

Model: DNN/new VGG16

## Sources:
https://doi.org/10.1038/sdata.2017.177

https://www.mdpi.com/2313-433X/5/3/37/pdf

https://arxiv.org/pdf/2008.12904.pdf

https://www.astesj.com/publications/ASTESJ_050220.pdf

Kamra A, Jain VK, Singh S, Mittal S. Characterization of Architectural Distortion in Mammograms Based on Texture Analysis Using Support Vector Machine Classifier with Clinical Evaluation. J Digit Imaging. 2016 Feb;29(1):104-14. doi: 10.1007/s10278-015-9807-3. PMID: 26138756; PMCID: PMC4722021.





