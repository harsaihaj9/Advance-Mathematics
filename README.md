# Predictive_Analytics_Advance_Mathematics

## Assignment: Probability Density Function Estimation using Roll-Number Parameterized Non-Linear Model

------------------------------------------------------------------------

## 1. Methodology

Data Collection → Column Selection → Data Transformation →\
Parameter Estimation → Probability Function Construction → Parameter
Reporting

------------------------------------------------------------------------

## 2. Description

-   **Dataset:** data.csv (India Air Quality Dataset)

-   **Target Column:** NO2

-   **Roll Number:** 102303957

-   **Transformation Formula:**

    z = T_r(x) = x + a_r sin(b_r x)

    where:

    a_r = 0.05 × (r mod 7)\
    b_r = 0.3 × (r mod 5 + 1)

-   For roll number 102303957:

    r mod 7 = 0\
    r mod 5 = 2

    Therefore:

    a_r = 0\
    b_r = 0.9

    Final transformation becomes:

    z = x

------------------------------------------------------------------------

## 3. Objectives

-   Perform transformation of the NO2 feature
-   Estimate parameters of probability density function
-   Apply estimation techniques (Mean & Variance based MLE)
-   Compute optimal values of parameters (λ, μ, c)

------------------------------------------------------------------------

## 4. Input Data

The dataset contains air quality measurements including:

-   stn_code
-   sampling_date
-   state
-   location
-   agency
-   type
-   so2
-   no2
-   rspm
-   spm
-   pm2_5
-   date

NO2 column is selected for analysis.

------------------------------------------------------------------------

## 5. Mathematical Model

The probability density function is defined as:

p(z) = c \* exp(-λ (z - μ)\^2)

Where:

μ = mean(z)\
σ = standard deviation(z)\
λ = 1 / (2σ²)\
c = sqrt(λ / π)

This form corresponds to a Gaussian distribution.

------------------------------------------------------------------------

## 6. Output (Estimated Parameters)

From computation:

Lambda (λ): 0.001460436524890011\
Mu (μ): 25.80962897811263\
C: 0.021560876239314918

------------------------------------------------------------------------

## 7. Visualization

A histogram of transformed data (z) is plotted along with the fitted
Gaussian curve using the estimated parameters.
<img width="297" height="201" alt="Screenshot 2026-02-18 at 10 34 02 AM" src="https://github.com/user-attachments/assets/d5812fe1-148a-4196-93c9-fa3fa1f3d2a4" />


------------------------------------------------------------------------

## 8. Conclusion

Since a_r = 0 for the given roll number, the nonlinear transformation
had no effect, and the model reduced to direct Gaussian estimation on
NO2 values.

The parameters were successfully estimated using statistical Maximum
Likelihood Estimation.

------------------------------------------------------------------------


