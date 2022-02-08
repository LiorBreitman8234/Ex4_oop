# Pokemon Game
![GIF](https://github.com/LiorBreitman8234/Ex4_oop/blob/master/Client/picturs/pokemon.gif)

------------------------------------------------
In this repository we present the fifth assignment of our OOP course as part of our B.sc in computer science. </br>

## Intro
In this assignment we get a graph, a number of agents, and pokemons. The goal of the game is to collect as much pokemons as we can in the time given to each level (0-15) </br>
We took the graph implementation from our [prevoius assignment](https://github.com/TaliaSeada/Ex3_OOP) </br>
For more information: [Assignment Ex4](https://github.com/benmoshe/OOP_2021/tree/main/Assignments/Ex4) </br>
In this assignment we combined all the assignments we had before.

----------------------------
## The Algorithm 
We took inspiration from our [first elevator assignment](https://github.com/TaliaSeada/Ex0_OOP) and [second elevator assignment](https://github.com/TaliaSeada/Ex1_OOP), 
and used the algorithms we build in our [first graph assignment](https://github.com/LiorBreitman8234/Ex2_oop) and [second graph assignment](https://github.com/TaliaSeada/Ex3_OOP).

First we seperated our algorithm into two cases, when we have one agent and when we have more than one agent.  </br>
In the first case, when we have only one agent, the algorithm is as follows: </br>
1. Create an empty list that will hold the nodes that the agent has to go through </br>
2. Iterate over all the pokemons and find the shortest path and distance from each one to the agent </br>
3. Sort all the pokemons according to their distance from the agent divided by the value </br>
4. 
   1. Insert the paths in a sorted way to the agent's list </br>
   2. If needed, insert the path between the destination of one pokemon to the source of the next one so we dont get stuck </br>


In the second case, when we have more than one agent, the algorithm is as follows: </br>
1. Create an empty list of lists, each one will hold the nodes that the corresponding agent need to go through </br>
2. Set a limit which will be the number of pokemons diveded by the number of agents rouneded down </br>
3. 
   1. Iterate over all the agents and for each one: </br>
   2. Iterate over all the pokemons and find the shortest path and distance from each one to the agent </br>
   3. Sort all the pokemons according to their distance from the agent divided by the value </br>
   4. While we are under the limit we set in step two we will pop from the start of the list of the pokemons </br>
   5. Insert the paths of the pokemons we popped in a sorted way to the agent's list </br>
   6. Mark the pokemons so that the next agents won't be assigned to them as well </br>

## Our Design Pattern 
![MVC](https://github.com/LiorBreitman8234/Ex4_oop/blob/master/Client/picturs/model-view-controller-light-blue.png)

<b> The Model: </b> </br>
The model defines what data the app should contain.</br>
If the state of this data changes, then the model will usually notify the view (so the display can change as needed) </br>
and sometimes the controller (if different logic is needed to control the updated view). </br>

<b> The View: </b> </br>
The view defines how the app's data should be displayed. </br>

<b> The Controller: </b> </br>
The controller contains logic that updates the model and/or view in response to input from the users of the app.

--------------------------------------
## Download and Run </br>
First clone the project. </br>
Next run the jar file like this: java -jar Ex4_Server_v0.0.jar __ </br>
&emsp; Instead of the underscore put a number between 0 and 15 (levels).

Last open the project in Pycharm and run the GUI file with a 3.8 python interpreter: </br>
&emsp; Edit the configuration by changing the 'Script path' to your local directory and specify to Ex4\Client\GUI.py

-----------------
## Results
Results for the 16 cases we got to test our algorithm
![Result](https://github.com/LiorBreitman8234/Ex4_oop/blob/master/Client/picturs/results.png)

------------------------
## Diagram
![Diagram](https://github.com/LiorBreitman8234/Ex4_oop/blob/master/Client/picturs/diagram.png)
