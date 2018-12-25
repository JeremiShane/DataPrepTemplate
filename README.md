# DataPrepTemplate
Template and repeatable process for data understanding and preparation

.R code files will be attached as a standard flow of exploratory analysis and preparation

# Basic Issues that must be resolved in Data Understanding
1. Data Collection
2. Data Description
  a.  Variables
  b.  Cases
  c.  Descriptive Statistics
3.  Quality
  a.  Missing
  b.  Outliers

# Data Preparation
1. Data Cleansing
2. Transformation
3. Imputation
4. Weighting and balancing
5. Filtering
6. Abstraction - How to handle temporal (time-series) data?
7. Data Reduction
  a. Sampling
  b. Dimensionality Reduction
  c. Discretization
8. Data Derivation - Can I create new variables?


# Data Description
 - Mean
 - Standard Deviation
 - Minimum
 - Maximum
 - Frequency tables - show the frequency distribution of values in variables
 - Histograms - graphical representation of frequency of values in variables
 
 # Data Assessment
  ## Data Profiling
      1. Data Distributions of each variable
        a. the central tendancy of data in each variable
        b. potential outliers
        c. number and distribution of blanks, nulls, NA's
        d. suspicious data like miscodes, test data, garbage
        
        *Cleans, filter and filter data that is too detailed for use in the modeling process
   ## Validation
      1. known codes
      2. proper ranges
      3. counts comparison to other sources
      4. proper formats
 
 # Data Transformations
  ## Numerical Data
    Many parametric statistical routines assume the effects of each variable on the target are linear.
    If using parametric modeling, have to transform any variables forming an exponential (non-linear) patter or curve.
    1. Standardazation - some models work best or require standardizing to a range
      a. common to use z-values = (value - mean) / standard deviation
        - the z scale ranges from + to - infiniti, but in a normal distribution 99.75% of values will lie between +3 and -3
      b. Standardize to +1 to -1 ...required by many SVM's
      c. 0 to 1 .... required by neural nets
   ## Categorical Data
      1. Dummy variables - this can improve the fit, but at a cost.  It reduces the degress of freedom by 1 every time you convert
      a variable to a set of dummy variables.  This reduces the generality of the model which can be more important than accuracy.
      2. numeric representation - can be used if there is a numeric increase in the impact across the range
   ## Feature Engineering
      - PCA
      - Kernel Density
  
 # Missing Data / Imputation
 
