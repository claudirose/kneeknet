# Datasheet Template

The dataset used in this project was sourced Kaggle https://www.kaggle.com/datasets/hafiznouman786/annotated-dataset-for-knee-arthritis-detection/data 

The original data is from Mendeley Data: Chen, Pingjun (2018), “Knee Osteoarthritis Severity Grading Dataset”, Mendeley Data, V1, doi: 10.17632/56rmx5bjcr.1 (see: https://data.mendeley.com/datasets/56rmx5bjcr/1)

## Motivation

The dataset was organised by the Osteoarthritis Initiative (OAI).

The OAI is a multi-center, ten-year observational study of men and women, sponsored by the National Institutes of Health (part of the US Department of Health and Human Services) as well as private pharmaceutical company partners managed by the Foundation for the National 
Institutes of Health. 

The goals of the OAI are to provide resources to enable a better understanding of prevention and treatment of knee osteoarthritis, one of the most common causes of disability in adults (ref:  https://nda.nih.gov/oai).

The acredited institution for the publically available dataset is the University of Florida. Pingjun Chen is the author. It is unclear whether this institution and author were involved in data collection or simply collation.
 
## Composition

The dataset consists of 1650 x-ray images of human knee joints. 

Each image has been classified according to standard KL (Kellgren and Lawrence) grading system:
- G0 Normal - definite absence of x-ray changes of osteoarthritis
- G1 Doubtful - doubtful joint space narrowing and possible osteophytic lipping
- G2 Mild - definite osteophytes and possible joint space narrowing
- G3 Moderate - moderate multiple osteophytes, definite narrowing of joint space, some sclerosis and possible deformity of bone ends
- G4 Severe - large osteophytes, marked narrowing of joint space, severe sclerosis and definite deformity of bone ends

(ref: https://radiopaedia.org/articles/kellgren-and-lawrence-system-for-classification-of-osteoarthritis)

There are 1650 images in the dataset in total. The class distribution is as follows:

- G0 Normal:  514 (31%)
- G1 Doubtful: 477 (29%)
- G2 Mild: 232 (14%)
- G3 Moderate: 221 (13%)
- G4 Severe: 206 (12%)

The majority of the images (89%) are of size (162 x 300) and show the x-ray of a single knee joint. However, the remaining images (size 161 x 640) are x-rays of both knees together. The split of these two sizes of x-rays are as follows:

G0 Normal :
- Two knees: 62 (4% of total)
- One knee: 452 (27% of total)
G1 Doubtful :
- Two knees: 37 (2% of total)
- One knee: 440 (27% of total)
G2 Mild :
- Two knees: 41 (2% of total)
- One knee: 191 (12% of total)
G3 Moderate :
- Two knees: 46 (3% of total)
- One knee: 175 (11% of total)
G4 Severe :
- Two knees: 0 (0% of total)
- One knee: 206 (12% of total)

The dataset contains sensitive and confidential medical information. However we have no information to link the images to the people. 

## Collection process

The exact collection process for the Knee Osteoarthritis Severity dataset is unknown to the author. However the general OAI study protocal is available on their website. It is assumed that this protocal was followed in the collection of the Knee Osteoarthritis Severity dataset.

The protocal states the general inclusion critea is:
- Men and women ages 45 – 79
- With, or at risk for, symptomatic femoral-tibial knee OA
- All ethnic minorities (focus on African-Americans)

And the major exclusion criteria is:
- Inflammatory arthritis (RA)
- Contraindication to 3T MRI
- Bilateral end-stage knee OA

The exact distribution of ages, ethnicities, sexes and risk factors in the Knee Osteoarthritis Severity dataset is unknown to the author. The timeframe over which the x-rays were taken is also unknown to the author, except for the fact that all images were taken prior to the dataset's release in September, 2018. 

It is unknown if the same individudal might appear across multiple images or categories.

## Preprocessing/cleaning/labelling

The raw data downloaded straight from Kaggle can be found in '.data/raw_data'

The images containing two knees have been removed. The purpose of this is to train the model on single-knee images only.

The 25% of the data across each category has been randomly chosen as test data and extracted into '.data/single_knee_images/test'. The remaining 90% of data is used for training and can be found in 'data/single_knee_images/train'. This split is arbitrary.

No other pre-processing or cleaning has been done.
 
## Uses

This publically avaiiable dataset shoud not be used for real classification of osteoarthritis because of the uncertainty of the exact collection process and distribution of ages, sexes, nationalities, ethnicities etc.

## Distribution

The dataset was originally distributed by Mendeley Data with the Creative Commons Attribution 4.0 International licence (CC BY 4.0). 

The CC BY 4.0 license means you can share, copy and modify this dataset so long as you give appropriate credit, provide a link to the CC BY license, and indicate if changes were made, but you may not do so in a way that suggests the rights holder has endorsed you or your use of the dataset. Note that further permission may be required for any content within the dataset that is identified as belonging to a third party. (ref: https://data.mendeley.com/datasets/56rmx5bjcr/1)

The dataset has also been distributed on Kaggle.  

## Maintenance

It is unknown to the author whether the publically available dataset will be maintained, or who it will be maintained by. No updates have been released since version 1 was made available in 2018. It is assumed that the OAI is responsible for maintaining and updating the original data. 

