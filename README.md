# 1. Introduction/Abstract

Bag of Visual Words is often used for image classsifcation.Its concept is derived from information retrieval and NLP’s bag of words concept. Features from the dataset images are used to construct vocabularies.Each image is then represented as a frequency histogram of features. From the frequency histogram, category of the test image is predicted. Feature of an image comprises of keypoints and descriptors. Keypoints are the unique 
points in an image.If the image is rotated, shrinked, or expanded, its keypoints will always 
be the same. Descriptor is basically the description of the keypoint. The main task of a 
keypoint descriptor is to describe an interesting patch in an image.  

  In this project we perform image classification on two datasets, using BoVW with SIFT feature detector.  Two classifiers i.e SVM and Random Forest are trained on both the datasets. First dataset is objects dataset consisting of 4 classes namely accordian, soccer ball, motorbike and dollar bill. The other is flowers dataset comprising of images from 5 classes named roses, dandelion,daisy,sunflower and tulip. Following is the methodology diagram followed for both the datasets for performing image classification. ![cv A1](https://user-images.githubusercontent.com/57056774/224492732-f5df3df6-e233-4644-9dfa-362e449c9bea.png)

 
  
  # 2. Instructions for installations
 If you are using google colab than packages are preinstalled, you just need to import them as
 ```bash
import cv2
import sklearn
import scipy
```  

 
 However while using local machine, use the package manager [pip](https://pip.pypa.io/en/stable/) to install opencv, scikit learn and scipy.

```bash
pip install opencv-python
pip install -U scikit-learn
python -m pip install scipy
```  
# 3. Instructions for running script
In order to run the script on google Colab:
1. Download the .ipynb file and upload it to colab. 
2. Download data sets and store them on drive individually.
3. Update the path locations in colab file according to your data path locations.
4. Execute the cells.


 # 4. Quantitative results
 
 ## Objects dataset
 For objects dataset following results were produced:
|                            |     SVM              |                     |                    |                      |     Random Forest    |                    |                    |                      |
|----------------------------|----------------------|---------------------|--------------------|----------------------|----------------------|--------------------|--------------------|----------------------|
|     Overall Accuracy       |     87.5             |                     |                    |                      |     100              |                    |                    |                      |
|                            |     'dollar_bill'    |     'accordion'     |     'motorbike'    |     'Soccer_Ball'    |     'dollar_bill'    |     'accordion'    |     'motorbike'    |     'Soccer_Ball'    |
|     F1 score               |     0.8              |     0.66666667      |     1              |     1                | 1                    | 1                  | 1                  | 1                    |
|     true positive rate     |     1                |     0.5             |     1              |     1                |     1                |     1              |     1              |     1                |
|     False positive rate    |     0.16666667       |     0               |     0              |     0                |     0                |     0              |     0              |     0                |
|     Accuracy               |     0.875            |     0.875           |     1              |     1                |     1                |     1              |     1              |     1                |

## Flowers dataset

 For flowers dataset following results were produced:
 |                            |     SVM        |                |                  |               |                   |     Random Forest    |                |                  |                |                   |
|----------------------------|----------------|----------------|------------------|---------------|-------------------|----------------------|----------------|------------------|----------------|-------------------|
|     Overall Accuracy       |     31.16      |                |                  |               |                   |     53.25            |                |                  |                |                   |
|                            |     roses      |      tulips    |     dandelion    |     daisy     |     sunflowers    |     roses            |      tulips    |     dandelion    |     daisy      |     sunflowers    |
|     F1 score               |     0.1939     |     0.44268    |     0.16574      |     0         |     0.26839       |     0.442211         |     0.6553     |     0.4336       |     0.56227    |     0.48044       |
|     true positive rate     |     0.12598    |     0.92307    |     0.11627      |     0         |     0.1937        |     0.34645          |     0.7417     |     0.379844     |     0.56428    |     0.5375        |
|     False positive rate    |     0.03600    |     0.7356     |     0.0607       |     0         |     0.06920       |     0.04582          |     0.17086    |     0.07881      |     0.10367    |     0.19377       |
|     Accuracy               |     0.8197     |     0.4268     |     0.79539      |     0.8102    |     0.7710        |     0.8495           |     0.8075     |     0.8265       |     0.8333     |     0.7479        |

# 5. Visual Results 
### Objects dataset
Following are the confusion matrices which were produced for svm and random forest in case of objects dataset:
![image](https://user-images.githubusercontent.com/57056774/224492978-4365b2e5-432e-4b1a-bcde-64332ed9ea03.png)  

Following are some of the images correctly classified by SVM.
![image](https://user-images.githubusercontent.com/57056774/224493379-d6584df6-136e-44a3-b5b2-d2a2add0f036.png)  

Following is the test image incorrectly identified by SVM.  
                ![image](https://user-images.githubusercontent.com/57056774/224493739-bcbee86f-46f7-499e-b474-b0d77a20503a.png)  


For Random forest all images were correctly classified.  
![image](https://user-images.githubusercontent.com/57056774/224494005-53fa5a41-bed7-4661-8163-ae38230cdb06.png)



### Flowers dataset

Following are the confusion matrices which were produced for svm and random forest in case of objects dataset:
![image](https://user-images.githubusercontent.com/57056774/224494210-4c1e9d3b-627f-40a8-8edc-aafbb9b75968.png)  

Following are some of the images correctly and incorrectly classified by SVM.
![image](https://user-images.githubusercontent.com/57056774/224494513-1cf00e1c-2572-4a8b-8f1c-732c5a06dc9f.png)    

Following are some of the images correctly and incorrectly classified by random forest.
![image](https://user-images.githubusercontent.com/57056774/224495916-0e3b68d4-581f-496c-9b18-e58bd81c493d.png)


# 6. Authors
Mariam Nasim - 399635






