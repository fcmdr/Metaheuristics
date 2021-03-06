# Metaheuristics Continuous and combinatorial optimization

## Discrete optimization

The Travel Salesman Problem is a well known problem in optimization. The goal is to find the shortest path linking all cities in a country for example.
http://www.math.uwaterloo.ca/tsp/world/countries.html#QA
This website contains the data of the tsp for some countries including the ones we tried to solve : Djibouti and Qatar.
If we tried to solve the problem with "brute-force" meaning by computing all the possibilities it will be very very long. All details (explanations and algorithm used) are in the corresponding jupyter notebook.
### Djibouti :
As an example in this case for the simpler problem "Djibouti" the number of possibilities is 38! which is approximately 5*10^44 possibilities. 
A genetic algorithm is proposed to solve this problem. The result was obtained relatively quickly in 6 minutes.
Here is the proposed path for Djibouti.

![Screenshot](/imgs/TSP_Djibouti.png)

### Qatar :
For Qatar the number of cities is 194 which is much higher than the previous example. In this case the number of possibilities is 194! which is really huge !
The same algorithm is kept to solve this problem however the result is less optimal 23730km whereas the best path distance is 9352km. There is certainly room for improvements to reach the optimal distance we may consider to use the 2-opt algorithm which is an deterministic approach.

![Screenshot](/imgs/TSP_Qatar.png)


## Continuous optimization

The goal of this exercise is to find the minimum of 6 differents functions in 50 and 500 dimensions.
The 2 first functions are unimodal (Shifted Sphere and Shifted Schwefel's problem).
The main algorithm used to optimize the differents functions is the BFGS (Broyden–Fletcher–Goldfarb–Shanno) algorithm which is a quasi-Newton method applied to a general 
function (that has not to be convex) that has continuous second derivatives. The jacobian and hessian of the function can be given to the algorithm if it is not the case it will approximate them. 
All of the details are in the differents notebook.

### Results of optimization for each function
### Function 1 Shifted Sphere :
![Screenshot](/imgs/Shifted_sphere_dim50.png)
![Screenshot](/imgs/Shifted_sphere_dim500.png)

### Function 2 Shifted Schwefel :
![Screenshot](/imgs/Shifted_Schwefel_dim50.png)
![Screenshot](/imgs/Shifted_Schwefel_dim500.png)


### Function 3 Shifted Rosenbrock :
![Screenshot](/imgs/Shifted_Rosenbrock_dim50.png)
![Screenshot](/imgs/Shifted_Rosenbrock_dim500.png)

### Function 4 Shifted Rastrigin :
![Screenshot](/imgs/Shifted_Rastrigin_dim50.png)
![Screenshot](/imgs/Shifted_Rastrigin_dim500.png)

### Function 5 Shifted Griewank :
![Screenshot](/imgs/Shifted_Griewank_dim50.png)
![Screenshot](/imgs/Shifted_Griewank_dim500.png)

### Function 6 Shifted Ackley :
![Screenshot](/imgs/Shifted_Ackley_dim50.png)
![Screenshot](/imgs/Shifted_Ackley_dim500.png)
