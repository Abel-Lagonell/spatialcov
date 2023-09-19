# spatialcov
spatial coverage

The goal of the spatial coverage project is to take a set of routes for a series of autonomous vehicles with on board sensors, and create a new set of routes for those vehicles with an increased diversity of routes taken while still having the same starting and ending points. This will increase the time spent making measurements with the sensors, and also increase the diversity of the sensing data obtained.

The first requirement is to create a random series of vehicle routes that adhere to real world expectations. For instance, back roads should have little traffic, while highways and intersections should have a greater density of vehicles traveling on them.

After creating the inital routes, the fréchet distances between each of the routes will need to be calculated, and this distance can be used to determine the diversity of the routes being taken. This diversity can in turn be used to determine the utility that each vehicle has on its original route.

With the utility of each vehicle calculated, a nash equilibrium can then be created that maximizes the utility of each vehicle by altering the paths taken for each vehicle's route.

### Updated Instructions
This shows the ubuntu commands that need to be done in order for a smooth installation

1  : Install Latest Ubuntu VM  

2  : ```sudo apt update```  
     ```sudo apt upgrade```  

3  : ```sudo apt install pip```  

4  : ```mkdir GitHub```  

5  : ```cd GitHub/```  

6  : ```sudo add-apt-repository ppa:sumo/stable```  
     ```sudo apt-get update```  
     ```sudo apt-get install sumo sumo-tools sumo-doc```  

7  : ```git clone [repository]```

8  : ```cd ./spatialcov```

9  : ```pip freeze > requirements.txt```  
     ```pip install -r requirements.txt```  
     ```sudo apt install libcairo2-dev pkg-config python3-dev```  
     ```pip install traci matplotlib pandas scipy seaborn scikit-learn dill networkx similaritymeasures```
     
10 : ```mkdir subscribe```
     ```cd ./subscribe```
     ```mkdir simulations```

11 : To run go back to the original files (```cd ../../```) in code and do ```python3 main.py```
