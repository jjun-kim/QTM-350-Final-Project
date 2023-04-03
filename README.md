# QTM-350-Final-Project
## Intro
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
