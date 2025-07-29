# Numerical Methods - Least Squares Regression Exercises
##### Created by Emir Yorgun

## Overview

This project focuses on implementing and analyzing **Least Squares Regression** techniques as part of a numerical methods exercise. It explores both **linear** and **polynomial regression** methods using Python, leveraging libraries such as **NumPy**, **SciPy**, and **Matplotlib**. The work is based on the methodologies outlined in the **"Python Numerical Methods" book** (Chapter 16), specifically sections on **direct inverse**, **pseudoinverse**, **NumPy linalg.lstsq**, and **polynomial regression for nonlinear functions**. The goal is to calculate the **total error (L2-norm)** between approximate and real values, applying these techniques to both synthetic and noisy datasets.

## Project Details

### Tasks and Implementation

1. **Environment Setup**: A Jupyter notebook was created to execute the analysis, providing an interactive environment for coding and visualization.
2. **Method Examination**: The project investigates three methods from the book:
   - **Direct Inverse Method**: Solves the least squares problem using the normal equation with matrix inversion.
   - **Pseudoinverse Method**: Utilizes **NumPy**'s linear algebra tools for a more robust solution.
   - **NumPy linalg.lstsq**: Employs a least squares solver for direct computation.
   These methods were studied, and their respective codes were executed to understand their behavior.
3. **Direct Inverse Application**: The **direct inverse method** was applied to a synthetic dataset with `x` ranging from 0 to 1 and noisy `y` values generated as `1 + x + x * random_noise`. The method constructs a matrix `A` with `x` and ones, computes the inverse, and derives coefficients `[1.58834249, 0.97466561]` to fit a **linear model**. A plot visualizes the data points and the fitted line.
4. **Polynomial Regression Analysis**: The **polynomial regression** technique was explored using a discrete dataset (`x_d` from 0 to 8, `y_d` with varying values). Polynomials of degrees 1 through 6 were fitted, and subplots were generated to compare the fits visually. The **L2-norm error** was calculated for each degree, showing a decrease from **1.3649 (degree 1)** to **0.1505 (degree 6)**, indicating improved accuracy with higher degrees.
5. **Error Calculation**: For the polynomial fits on the discrete dataset, the **total L2-norm error** was computed, with the lowest error (**0.1505**) at degree 6, suggesting a better fit as complexity increases.
6. **Noisy Data Application**: The **polynomial regression (degree 1)** was applied to the noisy dataset from the first section. The **L2-norm error** was **1.5709**, compared to **1.5709** from the linear regression, resulting in a negligible percentage change (**-1.41e-14%**), highlighting consistency between the methods for this dataset.
7. **Documentation**: The entire codebase, results, and analysis are compiled in a Jupyter notebook for submission, ensuring **reproducibility** and **clarity**.

### Datasets
- **Synthetic Data**: `x = np.linspace(0, 1, 101)` with `y_first = 1 + x + x * np.random.random(len(x))` for the **direct inverse method**.
- **Discrete Data**: `x_d = [0, 1, 2, 3, 4, 5, 6, 7, 8]` and `y_d = [0, 0.8, 0.9, 0.1, -0.6, -0.8, -1, -0.9, -0.4]` for **polynomial regression**.

### Results
- The **direct inverse method** provided a **linear fit** with coefficients indicating a slope of approximately **1.588** and an intercept of **0.974**.
- **Polynomial regression** demonstrated that higher degrees reduce the **L2-norm error**, with degree 6 offering the best fit among the tested polynomials.
- The noisy dataset analysis confirmed that a **simple linear model** suffices, with minimal error variation when compared to **polynomial regression**.


## Acknowledgements

This project draws inspiration from the **"Python Numerical Methods" book** available at [https://pythonnumericalmethods.berkeley.edu](https://pythonnumericalmethods.berkeley.edu). Special thanks to the resources and guidelines provided for facilitating this educational exercise.
