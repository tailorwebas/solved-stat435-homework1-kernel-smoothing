Download Link: https://assignmentchef.com/product/solved-stat435-homework1-kernel-smoothing
<br>
<strong>Gain experience with Kernel smoothing</strong>

<ul>

 <li> Write a R function</li>

</ul>

ksmooth.train(x.train, y.train, kernel = c(“box”, “normal”), bandwidth = 0.5, CV = False)

The kernels should be scaled so that their quartiles (viewed as probability densities) are at ±0<em>.</em>25 ∗ bandwidth.

The function should produce a list with components x.train and yhat.train.

If CV = True, training observation i should not be used in the calculation of yhat.train[i].

Do not assume that x.train is ordered. Try to be efficient!

<ul>

 <li>Write a R function predict(ksmooth.train.out, x.query)</li>

</ul>

The function should use linear interpolation inside the range ofx.train and constant extrapolation outside the range.

<strong>Note: </strong>Do not assume that x.query is ordered. Do not use the R function ksmooth.

I have randomly divided the Wage data from ISLR into a training set Wage.train of size 1000 and a test set of Wage.test of size 2000. The data are in the “dump” file home1-data.R that you can source.

<ul>

 <li>Produce a scatterplot of train vs age.train and add a kernel smooth for a normal kernel with bandwidth = 3. Print the residual sum of squares.</li>

 <li>Use the smooth computed above to predict test. Draw a scatterplot of wage.test vs age.test and add the smooth. Print the residual sum of squares.</li>

</ul>

1

<ul>

 <li>Plot the resubstition estimate of the expected squared prediction error as a function of bandwidth for bandwidths = 1, 2,…,10. Print the 10 values.</li>

 <li>Plot the LOOCV estimate of the expected squared prediction for the 10 bandwidths. and print the 10 values. What is the bandwidth you would choose?</li>

 <li>Plot the test set estimate of the expected suared prediction error for the 10 bandwidths and print the 10 values.</li>

 <li>Plot the 5-fold CV estimate of the expected squared prediction error for the 10 bandwidths and print the 10 values.</li>

</ul>

Use the assignment to training observations to folds defined by the variable fold in home1-data.R.