## Learning Probability Density Function using Roll-Number Parameterized Non-Linear Model

---

## Objective

The objective of this assignment is to learn the Probability Density Function (PDF) of a transformed variable derived from real-world air quality data. A roll-number-based non-linear transformation is applied to the NO₂ feature, and the resulting distribution is modeled using a Gaussian-like exponential function.

---

## Dataset

- **Feature Used:** NO₂ (Nitrogen Dioxide concentration)
- **Dataset:** India Air Quality Dataset
- **Source:** Kaggle  
  https://www.kaggle.com/datasets/shrutibhargava94/india-air-quality-data

---

## Step 1: Non-Linear Transformation

Each value of the feature \( x \) is transformed into \( z \) using:

\[
z = T_r(x) = x + a_r \sin(b_r x)
\]

Where:

- \( a_r = 0.05 \times (r \bmod 7) \)
- \( b_r = 0.3 \times (r \bmod 5 + 1) \)
- \( r \) = University Roll Number

This introduces controlled non-linearity into the dataset.

---

## Step 2: Probability Density Function Modeling

The transformed variable \( z \) is modeled using:

\[
\hat{p}(z) = c \cdot e^{-\lambda (z - \mu)^2}
\]

Where:

- \( \mu \) = Mean of the distribution  
- \( \lambda \) = Spread parameter  
- \( c \) = Normalization constant  

The parameters are estimated using curve fitting techniques.

---

## Tools & Libraries Used

- Python  
- Pandas  
- NumPy  
- Matplotlib  
- SciPy  

---

## Results

After applying the transformation and fitting the probability density function, the estimated parameters are:

- **μ (Mean)** = 25.80962289781127  
- **λ (Lambda)** = 0.0014604365254890003  
- **c (Normalization Constant)** = 0.021560876239314915  

These values define the learned probability density function for the transformed variable \( z \).

---

---

## Visualization

Below is the histogram of the transformed variable \( z \) along with the learned probability density function:

![PDF Learning Result](<img width="576" height="438" alt="Screenshot 2026-02-16 212711" src="https://github.com/user-attachments/assets/0f6985ea-6917-48a3-a1af-c1a5605ca6d4" />
)

The blue bars represent the histogram of the transformed data, and the red curve represents the learned Gaussian-based probability density function.

---

## Learning Outcomes

- Understanding non-linear transformations  
- Practical implementation of PDF estimation  
- Parameter optimization using curve fitting  
- Applying mathematical modeling to real-world environmental data  

---

## Conclusion

This assignment demonstrates how non-linear transformations impact data distributions and how probability density functions can be learned and modeled effectively using parameter estimation techniques.
