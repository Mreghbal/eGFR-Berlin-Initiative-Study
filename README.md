# Estimated Glomerular Filtration Rate (eGFR) Calculation using Berlin Initiative Study (BIS) Equation

Welcome to the README file for the eGFR calculation code based on the Berlin Initiative Study (BIS) equation. This code allows you to estimate the Glomerular Filtration Rate (GFR), which is a measure of kidney function, using the BIS equation. Below, you will find a detailed explanation of the subject, step-by-step instructions on how to run and use the code, and additional information to help you understand its purpose and applications.

## Table of Contents
- [Introduction](#introduction)
- [Explanation](#explanation)
- [Running the Code](#running-the-code)
- [Additional Information](#additional-information)
- [Follow Me](#follow-me)

## Introduction
The estimated Glomerular Filtration Rate (eGFR) is a widely used clinical parameter to assess kidney function. It provides an estimate of the volume of fluid filtered by the kidneys per unit of time. The Berlin Initiative Study (BIS) equation is one of the equations used to estimate eGFR. It takes into account factors such as age, gender, serum creatinine level, and race adjustment to calculate the eGFR value.

## Explanation
The eGFR calculation code is implemented in Python and consists of a function called `calculate_egfr`. This function takes four input parameters: `age` (in years), `gender` (either "male" or "female"), `serum_creatinine` (in mg/dL), and `race` adjustment factor (1 for non-black, 1.159 for black). It returns the calculated eGFR value in mL/min/1.73m².

The code follows these steps to calculate the eGFR:
1. Validate the input values to ensure they are greater than zero.
2. Check the gender input and assign the respective constants and multipliers based on the BIS equation.
3. Calculate the eGFR using the BIS equation, considering age, gender, serum creatinine level, and race adjustment factor.

To use the code, follow the steps outlined in the next section.

## Running the Code
To run the eGFR calculation code, please follow these steps:

1. Make sure you have Python installed on your system (version 3 or above).
2. Clone the repository or download the code files to your local machine.
3. Open a terminal or command prompt and navigate to the directory where the code files are located4. Run the following command to execute the code:
   ```
   python egfr_calculation.py
   ```
5. Follow the prompts to enter the required input values: age, gender, serum creatinine, and race adjustment factor.
6. After providing the input values, the code will calculate the eGFR and display the result.

Please note that the code assumes a serum creatinine unit of mg/dL and requires the race adjustment factor to be provided by the user depending on whether the patient is black or non-black.

## Additional Information
The eGFR calculation code based on the Berlin Initiative Study (BIS) equation provides a convenient way to estimate kidney function using readily available clinical parameters. It can be used in various medical settings, including nephrology, primary care, and research studies.

Here are some additional details to help you understand the code and its applications:

- **Berlin Initiative Study (BIS) Equation**: The BIS equation is a widely accepted method for estimating GFR. It takes into account factors such as age, gender, serum creatinine level, and race adjustment provide an estimate of kidney function.
- **eGFR Units**: The calculated eGFR value is expressed in mL/min/1.73m², which represents the volume of fluid filtered by the kidneys per minute adjusted for body surface area.
- **Input Validation**: The code validates the input values to ensure they are greater than zero. If any of the input values are invalid, an error message is displayed.
- **Exception Handling**: The code includes exception handling to catch and handle any errors that may occur during execution, such as invalid input values.
-LinkedIn and Twitter**: For more updates and information, please consider following me on [LinkedIn](https://www.linkedin.com/in/mreghbal) and [Twitter](https://twitter.com/mreghbal).

## Follow Me
If you find this code useful or have any questions, feel free to reach out to me. Don't forget to follow me on LinkedIn and Twitter for more updates and interesting projects.

LinkedIn: [Reza Eghbal](https://www.linkedin.com/in/mreghbal)

Twitter: [Reza Eghbal](https://twitter.com/mreghbal)
