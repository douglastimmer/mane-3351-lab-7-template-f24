# MANE 3351 - Manufacturing Engineering Analysis

## Laboratory 7 Assignment

#### Assigned: October 14, 2024

#### Due: October 23, 2024 (before 3:30 pm)

---

#### Learning Goals

1.  Vectorize function,
1.  Create arrays using Numpy, and
1.  Customize figures created with Matplotlib.

#### Description

This lab will utilize the standard (mu=0, sigma=1) largest value distribution introduced in Laboratory 6 to cover vectorizing functions, creating arrays using Numpy and customizing figures created with Matplotlib.

#### Step 1

Edit the first cell (markdown), to update your personal information.

#### Step 2

In cell two below the comment for step 2, vectorize the pdf function from Lab 6. Vectorizing a function was discussed in Lecture 11 on October 2.

*Steps 3 - 6 are based upon the Python code from a laboratory assignment from a previous course that is provided below. Instead of using the gumbel_l function from Scipy.Stats, you will use the vectorized function created in step 2. You will ask the user to input and store a value  (between -10 and +10).  You will modify the code so that you plot the pdf highlighting values greater than the inputted value.*


```python
from scipy.stats import gumbel_l
import numpy as np
import matplotlib.pyplot as plt

a=float(input("Enter the value of x: "))

x=np.linspace(-8,8,500)
y=gumbel_l.pdf(x,0,1)
y2=0.0*x
maske =(x<a)

plt.plot(x,y,'b')
plt.fill_between(x,y,color='#666666',where=maske)
plt.plot(x,y2,'b')
plt.show()
```

#### Step 3

In cell two below the comment for step 3, create an array named x using the Numpy linspace function that creates an array containing 500 points from -10 to +10.


#### Step 4

In cell two below the step 4 comment line, create the array y using the vectorized function created in step 2 and create the array y2 using the same code provided in the example code.

#### Step 5

In cell two below the step 5 comment line, ask the user to input a value b between -10 and +10. Create the array maske that contains values of True when X>b and False when X<b.

#### Step 6

Copy the code to create a plot from the sample code to cell two below the comments for step 6. You are to change the color for the line used to plot y and y2 versus x. [https://matplotlib.org/stable/gallery/color/named_colors.html](https://matplotlib.org/stable/gallery/color/named_colors.html) provides a list of base colors that can easily be used.

Modify the color of the fill from #666666 to any other value. [https://www.rapidtables.com/web/color/RGB_Color.html](https://www.rapidtables.com/web/color/RGB_Color.html) provides tools to pick a color. We are using the hex codes and not the RGB codes.

#### Step 7 

After running and testing your program, save the Jupyter Notebook. Upload your repository using GitHub desktop.