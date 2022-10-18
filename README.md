# DphiChallenge_DataSprint93_DryBeanClassification
## TensorflowModel and CSV Extractor for DataSci_Challenge  
Goal : Build ML model and make prediction for the types of beans corresponding to data  
(The prediction should be in a .csv file)  

Result(ID: waterloocanucks1) - 92.5% for public test and 	90.0667% for private test(test for ranking)  

# Tools

Tensorflow on Colab notebook
.csv files of dataset for training and test from Dhpi
***

# Specification

Optimizer is Adam optimizer and Loss function is Sparse Categorical Crossentropy.

And here is the summary of the model:  

![K-028](https://user-images.githubusercontent.com/84373345/196360266-5d3a7629-89e3-40e3-a40e-2da72d42878c.png)
***
# How I manipulated data to get rid of overfitting issue

As you see the dataset below, all values from some fieldnames are too small.  
So it was the main cause of the overfitting which makes the accuracy decrease to 25%.  

Multiplied by 1000000 when all values of certain column are below $10^{-2}$  
For the values from other columns which is below 1, multiplied by 10000 or 1000  
The values(x) from 0.99 to 0.98 are converted to the values((1-x)*1000000)  
To spread the values properly, for values of some columns, translations performed before enlarge the absolute values of data.  


![K-025](https://user-images.githubusercontent.com/84373345/196352158-a0afcbe6-718f-4b73-9481-fdc6ff812565.png)
![K-026](https://user-images.githubusercontent.com/84373345/196352160-2a113253-d502-4750-a564-fe5c5fb07c1b.png)
![K-027](https://user-images.githubusercontent.com/84373345/196352161-113ad839-bda7-4166-a204-fe280f3c893e.png)
***



Competition Link: https://dphi.tech/challenges/data-sprint-93-dry-bean-classification/298/data
## Overview
A computer vision system was developed to distinguish seven different registered varieties of dry beans with similar features in order to obtain uniform seed classification. Seven different types of dry beans were used in this research, taking into account the features such as form, shape, type, and structure by the market situation. For the classification model, images of 13,611 grains of 7 different registered dry beans were taken with a high-resolution camera. Bean images obtained by computer vision system were subjected to segmentation and feature extraction stages, and a total of 16 features; 12 dimensions and 4 shape forms, were obtained from the grains.

Your Task is to devise a Machine Learning model that classifies to which class each bean belongs to on the basis of the features provided.
***

## Evaluation

Evaluation Criteria  

Submissions are evaluated using Accuracy Score.  

Leaderboard:  

This challenge does partial evaluation.  

The initial/public leadeaboard is based on 50% of test data.  

The final results (private leaderboad) will be displayed after the challenge ends.  

The public leaderboard that is calculated during the competition evaluates only 50% of the test dataset,   whereas the private leaderboard will be calculated based on the remaining 50% dataset.   Hence, you might see some variation in ranks during and after the Datathon.  
***


## Dataset Description 

1. Area (A): The area of a bean zone and the number of pixels within its boundaries.  

2. Perimeter (P): Bean circumference is defined as the length of its border.  

3. Major axis length (L): The distance between the ends of the longest line that can be drawn from a bean.  

4. Minor axis length (l): The longest line that can be drawn from the bean while standing perpendicular to the main axis.  

5. Aspect ratio (K): Defines the relationship between L and l.  

6. Eccentricity (Ec): Eccentricity of the ellipse having the same moments as the region.  

7. Convex area (C): Number of pixels in the smallest convex polygon that can contain the area of a bean seed.  

8. Equivalent diameter (Ed): The diameter of a circle having the same area as a bean seed area.  

9. Extent (Ex): The ratio of the pixels in the bounding box to the bean area.  

10. Solidity (S): Also known as convexity. The ratio of the pixels in the convex shell to those found in beans.  

11. Roundness (R): Calculated with the following formula: (4piA)/(P^2)  

12. Compactness (CO): Measures the roundness of an object: Ed/L  

13. ShapeFactor1 (SF1)  

14. ShapeFactor2 (SF2)  

15. ShapeFactor3 (SF3)  

16. ShapeFactor4 (SF4)  

17. Class (Seker, Barbunya, Bombay, Cali, Dermosan, Horoz and Sira)  



