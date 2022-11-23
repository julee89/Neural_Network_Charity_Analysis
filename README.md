# Neural Network Charity Analysis

## Overview
The purpose of this anlaysis to predict whether a given applicant will be successful if funded by Alphabet Soup. Alphabet Soup has information on 34,000 organizations that have recieved funding from them and they are looking to use a binary classifier to perdict the success of a new applicant.

## Results
### Variables
Since this anlaysis is being conducted to understand the overall success of a candidate given the following variables listed below, we would need to consider IS_SUCCESSFUL as our target of the applicant being a candidate that will likely succeed with some confidence through our model.

- EIN
- NAME
- APPLICATION_TYPE
- AFFILIATION
- CLASSIFICATION
- USE_CASE
- ORGANIZATION
- STATUS
- INCOME_AMT
- SPECIAL_CONSIDERATIONS
- ASK_AMT
- IS_SUCCESSFUL

For the final model that had the most success we considered the following variables:
- AFFILIATION
- CLASSIFICATION
- USE_CASE
- SPECIAL_CONSIDERATIONS
- STATUS
- INCOME_AMT
- ASK_AMT

These variables seemed to be the most important in understanding the use of funds as well as who these applicants are aiming to target. In understanding the affiliation, classification and use case, we understand who this organization is aiming to target and given some organization will garner more public attention while others will not will be a huge determinant of success of the applicant. Then, there are risk factors which need to be considered when providing funds, therefore, we would need to gain some insight into who the applicant is and what financial risks they bring to Alphabet Soup. One of the main factors would be status to understand if the organization is still active or not, the income amout of the applicant or the organization and the amount of funding the organization is asking. Then, to catch some of the exceptions, we will include the special considerations that were given to some organizations at the discretiion of Alphabet Soup.

Then, the remainder of the variables are qualitative factors that will later shape the details of an organization or information that may be used to give special consideration, it would not be a quantitative factor we can rely on - these just create noise. And those variables are:

- EIN
- NAME
- APPLICATION_TYPE
- ORGANIZATION

### Compiling, Training, and Evaluating the Model
- This model has three hidden layers with 80, 30, 10 neurons respectively. The hidden layers in this deep-learning model use the activation function ReLU with the output being sigmoid since this is a binary model as shown in the code below

[Nodes](/Resources/nodes.PNG)

[Classification Bins](/Resources/class_bins.PNG)

[Application Bins](/Resources/application_bins.PNG)

To reduce additional noise with the classification of the applications and the types of applications, we increased the number of unique categories for these variables, which brought categories and application types to four and five bins respectively.

In increasing the layers, changing the nodes and reducing the bins our final optimized model had an accuracy score of 63.98%. Overall this model was not successful and there would need to be more optimization work done.

[Accuracy](/Resources/accuracy.PNG)

## Summary
Overall the optimized model for this dataset did not perform very well and will likely need to be adjusted or it would need to evaluated on a different model. Given, we are trying find a binary classifier, it would be worth it to look into a Random Forest model as well.
