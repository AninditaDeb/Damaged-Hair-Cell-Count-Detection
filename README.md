# Damaged-Hair-Cell-Count-Detection
Damaged Hair Cell Count Detection |DBSCAN| Hough Transform(Open CV)|Resnet with Context |Development Phase 

**Non Maximum and DB scan results**
![CApture1](https://user-images.githubusercontent.com/99614234/191880516-6a9d82d4-303a-4a25-9c0d-d418c8c4e304.PNG)

**Resnet Model Performance**

![Capture2](https://user-images.githubusercontent.com/99614234/191882006-3a7b5ce3-044a-4941-8b30-b1444c98dba4.PNG)


**Resnet Model with Context**
Trained two Resnet 18 models parallelly. Concatenated the feature map of last convolution layer and passed it to a fully connected layer for cell prediction.
![Capture3](https://user-images.githubusercontent.com/99614234/191881043-e4dbfa9e-d1b3-4676-8521-b3b170ad7228.PNG)

Model Performance after including conytext into it![Capture4](https://user-images.githubusercontent.com/99614234/191881306-28e0e1dc-ea14-4a41-aa69-5330954ab202.PNG)
