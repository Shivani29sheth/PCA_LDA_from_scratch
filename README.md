# PCA_LDA_from_scratch

## Problem statement

**Principal Component Analysis:**

Use all training images of three digits (‘4’, ‘7’ and ‘8’) in MNIST to estimate the principal component analysis (PCA) projection matrices, and then plot the total distortion error of these images as a function of the used PCA dimensions (such as 2, 10, 50, 100, 200, 300). Also, mention at least how many dimensions will you have to use in PCA in order to keep 98% of the total variance in data?

**Linear Discriminant Analysis:**

Use all training images of three digits (‘4’, ‘7’ and ‘8’) to estimate linear discriminant analysis (LDA) projection matrices for all possible LDA dimensions. What are the maximum LDA dimensions you can use in this case?

## Solution

**Principal Component Analysis:**

We perform Principal Component Analysis from scratch by computing the eigen values and variance of the image features. Once these are calculated, we plot them on a graph to analysize the top eigen values and the number of components required to keep maximum variance (about 98%) of the total variance in data.

<img src="PCA_LDA_Results/PCA_eignvalues.png" width="35%" height="35%">

<img src="PCA_LDA_Results/PCA_variance.png" width="35%" height="35%">

As per the 'Cumulative_explained_variance' graph shown above, we see that we need to use about 300 dimensions in PCA in order to keep 98% of the total variance in data.

Now, we also analyze the distortion in the reduced dimensional data by plotting the graph below:

<img src="PCA_LDA_Results/PCA_distortion.png" width="35%" height="35%">

Finally, after performing PCA we project all images into 2-D space and plot each digit in a different color for data visualization.

<img src="PCA_LDA_Results/PCA_plot.png" width="75%" height="75%">

**Linear Discriminant Analysis:**

In LDA, we can only use a maximum of 3 dimensions since we have only 3 class labels. Hence, using LDA, we would be able to separate the three classes in a maximum of 3 dimensions.

After performing LDA, we project all images into 2-D space and plot each digit in a different color for data visualization.

<img src="PCA_LDA_Results/LDA_plot.png" width="50%" height="50%">

Comparing the two data visualization methods, we see that the PCA method has a more spread out and overlapping visualization for the data point. This is because the PCA algorithm does not classify the data well based on their class labels. On the other hand, LDA is able to classify the data in a better way. We see that in LDA, we have more compact grouping of classes in the graph.
