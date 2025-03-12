# Handwritten Mathematical Expression Recognizer and Solver

The purpose of this project is to recognize and convert a handwritten mathematical expression from an image into its equivalent ASCII representation using a **Convolutional Neural Network (CNN)**.

The project is structured across three Jupyter Notebooks. The following sections outline its core components.

## Dataset Loading Function  
A function is defined to take as input a directory containing images and return a **normalized array**, adjusted according to the requirements of the model that will be defined later.

## Dataset Loading and Preprocessing  
Test and training datasets are constructed and populated. Each image in the dataset is assigned a corresponding label, which is initially included in the matrix and later extracted.

## Model Definition and Training  
A **sequential model** based on a **convolutional neural network (CNN)** is defined and then trained on the training dataset. Key metrics such as **loss** and **accuracy** are provided to assess the model's performance.

## Expression Recognition and ASCII Conversion  
The system processes expressions stored in the `"expressions"` folder:
1. Each expression is loaded sequentially.
2. The system **segments** the expression into individual components (e.g., numbers, operators).
3. A **prediction** is made for each component.
4. The final expression is reconstructed and displayed in **ASCII format**.

## Parsing and Result Calculation  
- If the recognized expression is **valid**, it is parsed and evaluated to compute the result.
- If the expression is **invalid**, an error message is displayed.
