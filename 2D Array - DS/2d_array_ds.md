## Question
[Question here](https://www.hackerrank.com/challenges/2d-array/problem)

## Explaining the solution

As the question explains, we have a 6 x 6 array (a 2-dimensional array). Our job is to iterate over the array until we can find all possible hourglasses (hint: they're sixteen in total!) and return the value of the maximum number of hourglasses possible. 

Take this for an example. Let's call the below array `arr`:
 
 arr = [
       [1, 2, 3, 4, 5, 6],
       [6, 5, 4, 3, 2, 1],
       [2, 3, 4, 5, 2, 1],
       [4, 3, 5, 6, 2, 4],
       [7, 8, 6, 4, 2, 1],
       [5, 6, 7, 8, 9, 9]
    ]

An example of a hourglass from arr[0][0] will be: 

[1, 2, 3],
   [5],
[2, 3, 4]

And the total value of that hourglass will be: 1 + 2 + 3 + 5 + 2 + 3 + 4 = `20`. 

We simply need to find all hourglasses in the entire 6x6 array and find the one with the highest value. 

To do this, we write a function that
1. Loops over each row in the 2d array
2. Loops over each column per row in the 2d array
3. Adds the values of the hourglass found therein. 
4. Compares the values to find out which one is the largest. 

Hence the code in the JavaScript solution in this folder. 

Hint; the -63 gotten as the max sum is actually the constraint supplied by the Hackerrank challenge. The minimum value of each item in the array is -9, which means the lowest possible hourglass is `-9*7 = -63`. 

[Credits](https://www.youtube.com/watch?v=0lajFzeFEFo) - written in Java. 
