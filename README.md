# matrix-multiplication
optimized matrix multiplication Dynamic Programming - Python

# Problem
Input: a chain of matrices to be multiplied<br>
Output: a parenthesizing of the chain<br>
Objective: minimize number of steps needs for the multiplication<br>

Suppose that we want to multiply a sequence of rectangular matrices. In which order should we multiply?<br>
 A x (BxC) or (AxB) x C

Matrices An n x m matrix A over the real numbers is a rectangular array of nm real numbers that are arranged in n rows and m columns. For example, a 3 x 2 matrix A has 6 

# Matrix Multiplication 
Let A be an n x m matrix B an m x p matrix The product of A and B is n x p matrix AB whose (i,j)-th entry is ∑k=1 m aik bkj In other words, we multiply the entries of the i-th row of A with the entries of the j-th column of B and add them up.

# Complexity of Matrix Multiplication
Let A be an n x m matrix, B an m x p matrix. Thus, AB is an n x p matrix. Computing the product AB takes nmp scalar multiplications n(m-1)p scalar additions for the standard matrix multiplication algorithm.

# Matrix Chain Order Problem
Matrix multiplication is associative, meaning that (AB)C = A(BC). Therefore, we have a choice in forming the product of several matrices. What is the least expensive way to form the product of several matrices if the naïve matrix multiplication algorithm is used? [We use the number of scalar multiplications as cost.]

# Why Order Matters 
Suppose we have 4 matrices: 
A: 30 x 1 
B: 1 x 40 
C: 40 x 10 
D: 10 x 25
 ((AB)(CD)) : requires 41,200 scalar multiplications<br>
 (A((BC)D)) : requires 1400 scalar multiplications<br>

# Matrix Chain Order Problem
Given matrices A1 , A2, …, An, where Ai is a di-1 x di matrix. [1] What is minimum number of scalar multiplications required to compute the product A1 · A2 ·… · An? [2] What order of matrix multiplications achieves this minimum? We focus on question [1], and sketch an answer to [2]

# A Possible Solution
Try all possibilities and choose the best one. Drawback: There are too many of them (exponential in the number of matrices to be multiplied) We need to be smarter: Let’s try dynamic programming!


# Dynamic Programming
A method for solving optimization problems <br>
DP is more efficient than other algorithms like greedy, divide and conquer, recursion,..<br>

# Featured point of DP
•	Get all the possible solution and pick up best and optimal solution.<br>
•	Work on principal of optimality.<br>
•	Define sub-parts and solve them using recursively.<br>
•	Less space complexity but more Time complexity.<br>
•	Dynamic programming saves us from having to recompute previously calculated sub-solutions.<br>
•	Difficult to understanding.<br>




