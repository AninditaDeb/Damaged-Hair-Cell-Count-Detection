# Damaged-Hair-Cell-Count-Detection
Damaged Hair Cell Count Detection |DBSCAN| Hough Transform(Open CV)|Resnet with Context |Development Phase 

•Created Bounding Boxes by template matching to identify the hair cells distributed across ring-like structures in hair follicles.
•Reduced the overlapping bounding boxes and selected the ones with the highest scores by implementing non-maximum suppression.
•Using the selected bounding boxes from the above step as coordinates of the centroid and performed DB SCAN which on further tuning  
 helped to categorize the true cells versus nontrue cells.
•Trained a Resnet Architecture from the input (from the above step)and a context with respect to every input which is basically a larger area of interest containing neighboring cells of the input to identify the cells more accurately.
•Reduced the false positives and false negatives by tracing back to the data and relabeling the positive and negative classes correctly.
•Trained the Resnet with the relabeled data in the first iteration and performed hard mining that increases the probability of selecting incorrectly identified samples from the first iteration as input to the Resnet in the second iteration and the same process follows in every iteration.
•Achieved an overall F1 score of 93% and accuracy of 97% test accuracy from correctly labeled and hardmined inputs.
•Implemented consensual collaborative filtering derived from Knowledge distillation to train the Resnet with context and obtained an overall performance of 
an average of 92% on test data compared to an average of 89% on test data with the same network without distillation.


**Non Maximum and DB scan results**
![CApture1](https://user-images.githubusercontent.com/99614234/191880516-6a9d82d4-303a-4a25-9c0d-d418c8c4e304.PNG)

**Resnet Model Performance**

![Capture2](https://user-images.githubusercontent.com/99614234/191882006-3a7b5ce3-044a-4941-8b30-b1444c98dba4.PNG)


**Resnet Model with Context**
Trained two Resnet 18 models parallelly. Concatenated the feature map of last convolution layer and passed it to a fully connected layer for cell prediction.


![Capture3](https://user-images.githubusercontent.com/99614234/191881043-e4dbfa9e-d1b3-4676-8521-b3b170ad7228.PNG)

Model Performance after including conytext into it

![Capture4](https://user-images.githubusercontent.com/99614234/191882125-083b9ad0-a31c-42a0-b91c-111306d3ecb0.PNG)


**Knowledge Distillation Frame work for Noisy Data**

 Teacher and Student Network
 
 ![Knowledge Distillation](https://user-images.githubusercontent.com/99614234/191882417-d7125213-1d8c-47f0-8efe-8aa732575a51.PNG)![Student Network](https://user-images.githubusercontent.com/99614234/191882595-a9d31441-25b6-40d2-84f1-51a83d74ae05.PNG)


