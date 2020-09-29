# P-Median-assignment
Assignment Relative of Discrete Optimization

IE 1144/IE 2144 – Discrete Optimization: Modeling and Computation
Dept. of Industrial Engineering University of Pittsburgh
Homework 1, due Date - September 28, 2020 before the start of the class
Please download the EXCEL file “Country Capital Cities” that contains countries/regions in the world and their capital cities (latitude and longitude, and populations). You can either use Julia or Python to read this file, process data and call Gurobi or CPLEX solver.
1 P-median Problem
For those 241 countries/regions, we are going to build a distribution network using P-median model. The distance between any two capital cities is the Euclidean distance, which can be computed as the following.
Given two points’ latitudes and longitudes, i.e., (lat, lng) and (lat0, lng0), and deglen := 110.25, we have
x:=lat−lat0; y:=(lng−lng0)∗cos(lat0)
distance := deglen ∗ sqrt(x2^2 + y2^2)
Let N denote the set of those capital cities, and cij denote the service cost (i.e., the Euclidean distance) between i,j ∈ N, and di be the demand (i.e., the population size) of i ∈ N. We will select p cities out of N to serve the distribution centers, and use the classical P-median model to complete this job.
(i) Please implement this model and compute your solutions for p=5,10,15,20,25,30, respec- tively using the MIP solver. Then, please draw a line in a figure showing the total cost vs. p.
(ii) Instead of using the MIP solver, we can develop a fast heuristic procedure to solve it. Please design and implement a fast heuristic procedure. In that figure, adding a new line to represent the total costs from your heuristic procedure. Please comment on the difference between those two lines.
2 More Advanced Modeling on P-median Problem
Please use p = 10 in this problem.
(i) If we have a distribution center in the first 20 capital cities, we must have at least one distri- bution center for capital cities 30 to 40. Modify and compute your model.
(ii) If the number of distribution centers in the first 20 capital cities is more than two, we must have at least one distribution center for capital cities 30 to 40. Otherwise, there is NO distribution center for capital cities 30 to 40. Modify and compute your model.
(iii) For capital cities of Canada (39) and USA (230), since they are close to each other, only one of those cities can be selected to build a distribution center. Modify and compute your model. (iv) It is required that either one distribution center will be built in capital cities of Canada (39)
or USA (230), or one distribution center will be built in capital cities of Mexico (139) or Panama (164). Note that only one situation will happen. Modify and compute your model.
(v) Sort those cities by their populations. For the top 10 cities with largest populations, it is required that no more than 3 distribution centers can be built. Modify and compute your model.
