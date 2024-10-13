# Alphabet Soup - Deep-Learning Challenge

# Background
This repository hosts a deep learning project for the nonprofit foundation Alphabet Soup, designed to predict the success of funding applicants. The foundation seeks a tool that can effectively select applicants with the highest likelihood of success in their ventures. Leveraging your expertise in machine learning and neural networks, you will utilize a dataset provided by Alphabet Soup, which includes a CSV file containing over 34,000 organizations that have previously received funding.

## Overview of the Analysis

The project focuses on creating a binary classifier to identify successful applicants from a dataset using various features. The primary steps include designing a neural network model with TensorFlow, compiling and training it to assess its effectiveness in predicting applicant success, and refining the model through iterative adjustments. This tool aims to improve funding decisions for Alphabet Soup by accurately predicting which applicants are likely to succeed if granted funding.

The analysis begins with data preprocessing, which involves eliminating unnecessary columns, encoding categorical variables, and dividing the dataset into training and testing sets. Following this, a neural network model is constructed, trained, and evaluated for loss and accuracy. Optimization techniques are employed, including refining input data, altering network architecture, adjusting activation functions, and modifying training epochs to enhance model performance.

The ultimate objective is to achieve predictive accuracy exceeding 75%. Once the model is optimized, it will be saved as an HDF5 file for future applications.

## Results

### Data Preprocessing

1. What variable(s) are the target(s) for your model?
 The target variable for the model is `IS_SUCCESSFUL`, a binary variable indicating the charity project was successful (`1`) or not (`0`).

2. What variable(s) are the features for your model?
 All columns, with the exception of EIN, NAME, and IS_SUCCESSFUL, function as features for the model. These encompass a range of attributes related to the charity projects and the organizations that support them.

3. What variable(s) should be removed from the input data because they are neither targets nor features
 The EIN and NAME fields were excluded from the dataset as they are identifiers that do not aid in predicting project success. They lack relevant information that would enhance the model's predictive capabilities.


### Compiling, Training, and Evaluating the Model

1. How many neurons, layers, and activation functions did you select for your neural network model, and why? 
The final neural network architecture features three hidden layers containing 128, 64, and 32 neurons, respectively.
 Initially, the model began with a simpler design, utilizing fewer neurons and layers. However, to better capture complex patterns in the data, the architecture was enhanced, resulting in improved performance.

2. Were you able to achieve the target model performance?
The target was to achieve an accuracy of at least 75%. Unfortunately, after multiple optimization attempts, the final model achieved an accuracy of 73% on the test dataset.

3. What steps did you take in your attempts to increase model performance?
Expanded Neurons and Layers: Initially, the model was quite basic, but it evolved into a more sophisticated structure by incorporating additional neurons and layers. This enhancement enabled the model to identify more intricate patterns within the data.
 Refined Activation Functions: The ReLU activation function was selected for the hidden layers due to its effectiveness in deep learning applications.

## Summary

### Overall Results
The final deep learning model reached an accuracy of 73%, which is below the desired target of 75%. Although the model demonstrates some ability to predict the success of charity projects funded by Alphabet Soup, its accuracy is insufficient for making reliable funding decisions. As it currently stands, the model may not serve as the most effective tool for informed funding choices.

To enhance the model's performance and potentially achieve or exceed the target accuracy of 75%, consider implementing the following fine-tuning strategies:

- Increase Neurons per Layer:
Augmenting the number of neurons in each layer may improve the model's capacity to capture complex relationships present in the dataset.

- Test Different Activation Functions:
Explore various activation functions, such as Leaky ReLU or ELU, as they might yield better results than the standard ReLU in specific contexts.

By applying these strategies, you can enhance the model's accuracy, making it a more effective tool for predicting the success of charity projects and aiding Alphabet Soup in its funding decisions.
