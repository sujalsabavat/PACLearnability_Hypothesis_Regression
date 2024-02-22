# Problem Statement
## TASK 1: Harmony in Frames 
(a) Consider the set of sorted points  x1,x2,…,xn  sampled independently and identically from Uniform distribution from range  0  to  1 . For simplicity, let us look into problem where corresponding labels ( yi ) to each  xi,∀i∈[n]  is either positive ( 1 ) or negative ( 0 ).

(b) Further, consider a class of hypothesis ( Hk ) that consider countable union of  k  non-overlapping partitions (called frames). Particularly, for instance a set of such partitions is denoted as  P={[a1,b1],…,[ak,bk]  where  0≤a1≤b1≤a2≤…≤ak≤bk≤1 . 
Then any hypothesis  hP∈Hk  is given as
hP={1    if x∈[a1,b1] or [a2,b2] or …,[ak,bk]0    otherwise  

(c) As you have a collection of data points  (x1,y1),…,(xn,yn)  where  xi 's are uniformly distributed on space  0  to  1 , let us now look into probability distribution of labels  yi 's to each of the  xi 's i.e., the true distribution  P(x,y)=P(y|x)P(x)  is given as below:

P(y=positive|x)={0.7   if x∈[0,0.2]∪[0.4,0.6]∪…,[0.8,1]0.2   if x∈(0.2,0.4)∪(0.6,0.8) 

and  P(y=negative|x)=1−P(y=positive|x) .



Now, as you have gathered complete prerequisite knowledge for the question, let us look into the sub-tasks which needs to be performed as part of this lab assignment.

We have provided you with a snippet [called PartitionRaja_Discover( ⋅ )] that returns the best possible tuple of  k  partitions on given sorted list of  X  values and corresponding labels  Y  for a fixed  k .

SubTask 1: Code the procedure SUBTASK1 that takes as input a list of partitions  P , computes the true error and empirical error.
Now, fix  k = 3  and vary number of data points  n=10,20,…,200 . For each value of  n  find the mean and standard deviation of emprirical, true error over 10 independent runs. Plot these both error values against  n .


SubTask 2: Sample a dataset of size  n=1500 . Find the best emprical risk minimizer hypothesis using code snippted provided for different  k  values from  1,2,3,…,10 . Plot the mean and standard deviation of emprirical, true error over 10 independent runs. Plot these both error values against  k .
## Task 2: Gaussian and Poisson Noise
In this question, we will test the effect of different noise on the polynomial curve fitting with regression.

Let the given function is  f(x)=2cos(x)−π+(2x)(2π)+2cos(3x)(−3π)+(z×Noise ) where  x  ranges from  −10  to  10  and  z  is the scaling factor for the additive noise.

Noise ∼N(μ=0,σ=1)  and added with a scaling factor of 0.1 in the function f(x). Perform the next steps using gaussian noise.

a. Generate  50  data points from the given f(x) and gaussian noise. 
b. Fit a polynomial regresser for the above generated data using gradient descent optimizer with momentum .

Try it with multiple degrees of polynomial  M  where  M  = [1,20] and report the empirical error for each  M . 

c. Report the best and worst fit degree along with proper observations and graphs. 

d. Repeat the previous experiments with more number of data points and report your findings. 

e. Plot the bias and variance with respect to  M . 
f. Plot the bias and variance with respect to number of datapoints. 

Noise ∼P(λ=2)  and added with a scaling factor of 0.1 in the function f(x). Perform the next steps using poisson noise.

a. Generate  50  data points from the given f(x) and possion noise. 
b. Fit a polynomial regresser for the above generated data using gradient descent optimizer with momentum. (Already graded) Try it with multiple degrees of polynomial  M  where  M  = [1,20] and report the empirical error for each  M . 
c. Report the best and worst fit degree along with proper observations and graphs. 
d. Repeat the previous experiments with more number of data points and report your findings.
e. Plot the bias and variance with respect to  M .
f. Plot the bias and variance with respect to number of datapoints. 

Compare for both types of noise added to the function f(x) and report your observations. 

Note: Code the gradient descent from scratch for full credit. 50% marks will be deducted if you use inbuilt library functions for optimizer and regression.

## Task 3:  Hypothesis 
 Given a concept class  h  which comprises of axis-aligned rectangles with  a≤x≤b  and  c≤y≤d  where  a ,  b ,  c ,  d  are real numbers with condition 0  ≤p≤q≤  100 and 0  ≤r≤s≤  100. Implement the following:

Generate a random concept  h  with  p,q,r,s  parameters for a rectangle.

Generate a dataset with atleast 100 i.i.d samples ( x , y ) drawn from uniform distribution. Label them with the generated concept  h  in the previous step. The samples inside the rectangle should be labelled as 1 and 0 otherwise. The points on the boundary of rectangle should be labelled as 1. 
Note: Make sure to have good enough points for both labels 1 and 0.

Write a function to generate the hypothesis  h1  for the given data and calculate its empirical error. 
Plot the concept  h  (true hypothesis) and generated hypothesis  h1  on the generated data. 
Now, again sample 100 more points from the uniform distribution and check the empirical error with hypothesis  h1 . 
Add these 100 samples from step 5. in the original dataset, and reestimate the hypothesis  h2  and calculate error on  h2 . 
Plot  h ,  h1  , h2  on the dataset and report your observations. 



