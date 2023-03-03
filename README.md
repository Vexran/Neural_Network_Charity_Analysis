# Neural_Network_Charity_Analysis

## Overview

This analysis aimed to explore and implement neural networks using TensorFlow in Python. Neural networks are an advanced form of Machine Learning that can recognize patterns and features in the dataset. Neural networks are modeled after the human brain and contain layers of neurons that can perform individual computations. A great example of a Deep Learning Neural Network would be image recognition. The neural network will compute, connect, weigh, and return an encoded categorical result to identify if the image represents a "dog," a "cat," etc.

AlphabetSoup, a philanthropic foundation requests a mathematical, data-driven solution to help determine which organizations are worth donating to and which are considered "high-risk." In the past, only some donations AlphabetSoup has made have been impactful, as there have been applicants that will receive funding and then disappear. Beks, a data scientist for AlphabetSoup, is tasked with analyzing each donation's impact and vetting the recipients to determine if the company's money will be used effectively. To accomplish this request, we are tasked with helping Beks create a binary classifier to predict whether an organization will succeed with its funding. We utilize Deep Learning Neural Networks to evaluate the input data and produce precise decision-making results.

## Results
We used a CSV file containing more than 34,000 organizations that have received past contributions over the years. The following information was contained within this dataset.

CSV contains over 34,000 organizations that have received funding from Alphabet Soup. Within this dataset are several columns that capture metadata about each organization, such as the following:

EIN and NAME—Identification columns APPLICATION_TYPE—Alphabet Soup application type AFFILIATION—Affiliated sector of industry CLASSIFICATION—Government organization classification USE_CASE—Use case for funding ORGANIZATION—Organization type STATUS—Active status INCOME_AMT—Income classification SPECIAL_CONSIDERATIONS—Special consideration for application ASK_AMT—Funding amount requested IS_SUCCESSFUL—Was the money used effectively
![data stuff](https://user-images.githubusercontent.com/113754027/222620229-e12b81e4-2bbd-4fa5-b050-4b059cf3c365.png)
Attempts to Optimize and Improve the Accuracy Rate Three additional attempts were made to increase the model's performance by changing features and adding/subtracting neurons and epochs. The results did not show any improvement. 

<img width="368" alt="woah data" src="https://user-images.githubusercontent.com/113754027/222620371-6a134540-5e39-4179-9c79-0bd737cbcec7.png">

Optimization Attempt #1:

Binned INCOME_AMT column
Created 5,821 total parameters, a decrease of 160 from the original 5,981
Accuracy improved by 0.13% from 72.50% to 72.63%
The loss was improved by 2.14% from 57.92% to 60.06%
Optimization Attempt #2:

Removed ORGANIZATION column
Binned INCOME_AMT column
Removed SPECIAL_CONSIDERATIONS_Y column from features as it is redundant to SPECIAL_CONSIDERATIONS_N
Increased neurons to 100 for the first hidden layer and 50 for the second hidden layer
Created 8,801 total parameters, an increase of 2,820 from the original 5,981
Accuracy decreased by 0.20% from 72.50% to 72.30%
The loss increased by 1.01% from 57.92% to 58.93%
Optimization Attempt #3:

Binned INCOME_AMT and AFFILIATION column
Removed SPECIAL_CONSIDERATIONS_Y column from features as it is redundant to SPECIAL_CONSIDERATIONS_N
Increased neurons to 125 for the first hidden layer and 50 for the second hidden layer
Created 11,101 total parameters, an increase of 5,120 from the original 5,981
Accuracy decreased by 0.03% from 72.50% to 72.47%
Loss decreased by 0.11% from 57.92% to 57.81%

## Summary
In summary, our model and various optimizations did not help to achieve the desired result of greater than 75%. With the variations of increasing the epochs, removing variables, adding a 3rd hidden layer (done offline in Optimization attempt #4), and/or increasing/decreasing the neurons, the changes were minimal. They did not improve above 19 basis points. Reviewing other Machine Learning algorithms, the results did not prove any better. For example, Random Forest Classifier had a predictive accuracy rate of 70.80%, a 1.70% decrease from the accuracy rate of the Deep Learning Neural Network model (72.50%).

Overall, Neural Networks are very intricate and would require experience through trial and error or many iterations to identify the perfect configuration to work with this dataset. 
