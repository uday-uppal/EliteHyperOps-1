# EliteHyperOps
Create_Dataset.py is used to generate data on which we train the Neural Network in train.py file. The reason we are training the Neural Network , instead of using the actual Frank Wolfe is because FW is computationally expensive. And in our end goad to detect braess routes we need to apply it multiple times. A well trained NN will give us lower computational cost and make our solution realtime.

Graph.py and Model.py are the File that contain actual Franke Wolfe Algorithm Implementation. Example.py is used to combine them and run actual Franke Wolfe Algorithm. Data.py contains all the data(like graphs, demand, capacity, potential routes that need to be checked for braess routes(braess indexes)) which corresponds to Hyperloop Station in Pune. frank_wolfe_nn is our trained Neural Network. Presently it is trained on 3100 data points with average loss of 8.170. Main.py uses the trained Neural Network to output the Braess Routes. Here, we have searched for braess routes only in links between the Hyperloop Platforms, because these routes that have the highest concentration of traffic during peak hours. But our software is eqully capable of scanning the whole network for these braess routes. 

How to use it in Hyperloop Station.
1) Given demand and capacities  at a particular instant of time, our software outputs braess routes, in a network of routes which act as bottlenecks and hence need special attention.
2) These braess routes are a function of demand and time. That is, braess routes change from time to time as demand of people using a particular route changes. Hence we would need to run the software first with the predicted demand of each routes, using ticketing information and then using realtime data from Mobile Signals,and CCTV cameras.
3) We would use these braess routes, till they "just" start acting as bottle necks ,following which, we would disincentivise them. This can be done by changing direction on LED Sign Boards, and notifying the user on an app which would tell them most optimised routes. Using the principle of collective intelligence, we would tell every passenger the routes which would be best for the overall traffic condition, and not necessarily the shortest path for that particular individual.  .

Hence, Our Software can revolutionalize how we tackle the problem of Traffic Management.  

graph.py, model.py taken from this [awesome repo](https://github.com/ZhengLi95/User-Equilibrium-Solution) by [ZhengLi95.](https://github.com/ZhengLi95)
