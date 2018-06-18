# Multi-unit production planning with integer and continuous variables (hard penalty approach)   
##### An optimization test suite involving 162 integer and 108 continuous variables

This submission can be used to evaluate the performance of optimization techniques on problems with integer and continuous variables. This optimization problem arises for maximization of profit in production planning. However these files can be used as black-box optimization problems.

There are eight minimization optimization problems in this suite (case1.p, case2.p, case3.p, case4.p, case5.p, case6.p, case7.p and cas8.p). All the cases have a problem dimension of 270 variables. The first 162 variables are integer (if not, then rounded using MATLAB inbuilt round function) whereas the remaining 108 variables are continuous. 

Each of them follows hard penalty approach and  has the following format
```
[ F ] = case1(X);
```
Input: population (or solution, denoted by X) and its 
Output: objective function values (F) of the population members.

The file ProblemDetails.p can be used to determine the lower and upper bounds along with the function handle for each of the cases.

The format is `[lb, ub, fobj] = ProblemDetails(n);`

Input: n is an integer from 1 to 8. 
Output: (i) the lower bound (lb), 
(ii) the upper bound (ub), and 
(iii) function handle (fobj).

The file Script.m shows how to use these files along with an optimization algorithm (SanitizedTLBO).


**Note:** <br> 
  1. Case 1 - 4 have the same problem structure but employ different data; Case 5 - 8 has same set of data as compared to Case 1 - 4, but do not employ a certain feature (flexible) of the problem.

  2. The objective function files are capable of determining the objective function values of multiple solutions (i.e., if required, the entire population can be sent to the objective function file).
