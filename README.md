# Non-Linearity Index
This is a fun idea that I've had in the back of my mind for the past 4 months or so, that I finally got around to coding. The main question that this code seeks to answer is how linear your dataset is. This can be useful when trying to determine whether to use a linear method such as regression, LDA, and Logistic Regression among many others instead of say a Support Vector Machine or a Random Forest.

# Algorithm
The first step is to measure the datasets intrinsic dimension. In this implementation I use the skdim.id.TwoNN() function to do this. Once you know this then you can run pca and see how much variance is explained by the same number of components as there are intrinsic dimensions. If the number is close to 1 it means that the data is linear. If the number is closer to 0 then it means that the data is non-linear.

# Disclaimer
This metric has yet to be tested to ensure that it behaves exactly as described. It is possible, and even likely that playing with hueristic could lead to improvements. This is more of a fun idea that with a bit more work could be useful.
