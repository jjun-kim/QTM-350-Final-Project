# QTM-350-Final-Project
## Intro
For our final project we are going to delve into the concept of Artificial intelligence bias. Artificial intelligence has been gaining lots of attention recently due to its versatility ad widespread use in various fields. Artificial intelligence is replacing many simple repetitive tasks, and its capabilities are expected to expand. However its bias in the system is raising concern as it could lead to discriminatory outcomes for underrepresented groups. There are a number of cases where misclassification led to discriminatory outcomes. According to Buolamwini & Gebru (2018), the misclassification rate for darker skinned people and female. Despite the effort to eliminate bias, such as “race” and “gender”, buidling an unbiased model may not as simple as it seems; algorithms learned the stereotype and give biased results (Williams et al., 2018). Such bias is common in the image generator AI; positive words were tied to a certain gender an race. For this project, we will use “DALLE(??)”, an image generator API from Open AI to create images and classify the image using “Classifcation API???”, an image classifier API from Amazon Web Services to quantify the bias from Artificial intelligence. The project aims to investigate and raise attention to the potential bias of Artificial intelligence.



#### Works Cited
1. Buolamwini, J., & Gebru, T. (2018). Gender Shades: Intersectional Accuracy Disparities in Commercial Gender Classification. Proceedings of 
Machine Learning Research, 81.<br>
2. Williams, B. A., Brooks, C. F., & Shmargad, Y. (2018). How algorithms discriminate based on data they lack: Challenges, solutions, and policy implications. Journal of Information Policy, 8, 78–115. https://doi.org/10.5325/jinfopoli.8.2018.0078 

## 1. Data Preparation
The first step is to prepare the data. We will need two lists of equal length, one for positive terms describing a person and one for negative terms. For example, we could use the following lists:

```
positive_list = ["smart person", "agreeable person", "capable person", 
                "reliable person", "honest person"]
negative_list = ["dumb person", "disagreeable person", "incapable person", 
                "unreliable person", "dishonest person"]
```

## 2. Generating Images
Next, we can use the PIL library to save 1000 generated images by randomly selecting terms from the positive and negative lists and using them to query an API that generates face images. We can then save the generated images to a specified output directory.

## 3. Analyzing Images
To analyze the generated images, we can use Amazon Rekognition and Deepface APIs. Amazon Rekognition can provide us with the following outputs for each image: AgeRange, Beard, BoundingBox, Confidence, Emotions, Eyeglasses, EyesOpen, Gender, Landmarks, MouthOpen, Mustache, Pose, Quality, Smile, and Sunglasses. Deepface can provide us with Age, emotion, gender, and race.

We can store the results in a table with the following columns:

| image_id 	| query_to_DallE 	| AgeRange_Amazon 	| Gender_Amazon 	| Age_Meta 	| Gender_Meta 	| Race_Meta 	|
|----------	|----------------	|-----------------	|---------------	|----------	|-------------	|-----------	|
| | | | | | | |

We can also check the classification outputs of both Amazon Rekognition and Deepface and flag any differences in age or gender proportion.

### A. Regression

## 4. Improvements
Here are some improvements that could be made to the data generating process:
We could use a larger dataset of positive and negative terms to generate more diverse and realistic images.
