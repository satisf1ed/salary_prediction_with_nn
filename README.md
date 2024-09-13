# Job Salary Prediction

This project focuses on predicting salaries for various job positions based on multiple features, including job title, job description, and other categorical attributes. The dataset used in this project contains various job-related information, with the salary being the target variable to predict.

## Project Overview

The goal of this project is to build a machine learning model that accurately predicts the salary of a job based on its title, description, and other categorical features. To achieve this, a custom neural network (NN) with a three-head architecture was developed:

1. **Job Title Head**: Processes the job title feature.
2. **Job Description Head**: Processes the job description feature.
3. **Other Features Head**: Processes other categorical and numerical features.

The outputs from these three heads are concatenated and passed through additional layers to generate the final salary prediction.

## Dataset

The dataset used in this project includes the following features:

- **Job Title**: The title of the job position.
- **Job Description**: A detailed description of the job responsibilities and requirements.
- **Other Categorical Features**: Additional attributes such as company, location, industry, etc.
- **Salary (Target)**: The target variable representing the salary to be predicted.

## Model Architecture

The custom neural network consists of three separate heads, each processing a specific type of input:

![Screenshot 2024-09-13 at 15 05 31](https://github.com/user-attachments/assets/746ad58f-e04c-411d-921e-801cea748ab7)

- **Head 1: Job Title Processing**:
  - An embedding layer to handle categorical job titles.
  - A series of convolutional to capture context and semantics.
  - Dense layers to extract meaningful patterns from job titles.

- **Head 2: Job Description Processing**:
  - Text preprocessing layers (tokenization, embedding) to handle the job description.
  - A series of convolutional to capture context and semantics.
  - Dense layers to extract meaningful patterns from job titles.

- **Head 3: Other Features Processing**:
  - Dense layers to process and learn from other categorical or numerical features.

The outputs of these three heads are concatenated and passed through fully connected layers to produce the final salary prediction.

## Installation

To run the project, you need to have Python 3.x installed along with the following libraries:

- PyTorch
- Pandas
- NumPy
- Scikit-Learn
