# MDP REPRESENTATION

## AIM:
To represent a Markov Decision Process(MDP) problem in the following ways.
1) Text representation
2) Graphical representation
3) Python - Dictonary representation
## PROBLEM STATEMENT:
To develop an environment in which a person is going for a picnic. The goal is to reach the picnic spot without getting lost.
## Problem Description
The agent has to reach the goal state(picnic spot) by taking the correct step towards the goal without drifting away from the path. After reaching the goal the agent will be rewarded if not then no reward will be provided.
## State Space:
{0,1,2,3}
## Sample State:
0 -> Starting point(S)
1 -> Relaxing point(R)
2 -> Picnic point(G)
3 -> Restricted point(D)
## Action Space:
{1,2}
## Sample Action:
1 -> Moving up
2 -> Moving down
## Reward Function:
If Agent reached Goal(G) state:
reward=+1
else
reward=0
### Graphical Representation:
![image](https://github.com/swethamohanraj/mdp-representation/assets/94228215/ca71410a-bc7d-4cd5-91a2-a21d7ece275e)

## PYTHON REPRESENTATION:
```
Picnic = { 
    #starting point state(S) ->0
    #Action: up-> 1, down-> 2
  0:{
     1:[(0.82 , 1 , 0,False),(0.18 , 0 , 0 , False)],
     2:[(0.88 , 0 , 0,False),(0.12 , 1 , 0 , False)] 
  },
    #Relaxing point state(R) ->1
  1:{
     1:[(0.91 , 2 , 0,False),(0.09 , 0 , 0 , False)],
     2:[(0.75 , 0 , 0,False),(0.25 , 2 , 0 , False)]
  },
    #Picnic point state(G) ->2
  2:{
      1:[(0.92 , 3 , 1,True),(0.08 , 1 , 0 , False)],
      2:[(0.91 , 1 , 0,False),(0.09 , 3 , 1 , True)]
  },
    #Restricted point(R) ->3
  3:{
      1:[(0.82, 3 , 0, True),(0.18 , 2 , 0 , False)],
      2:[(0.73, 2 , 0, False),(0.27 , 3 , 0 , True)]
  }
}
Picnic
```
## OUTPUT:
![image](https://github.com/swethamohanraj/mdp-representation/assets/94228215/3629fcbd-bcaa-4bec-834a-359674733e9a)

## RESULT:
Hence we have created an environment suitable for the above mentioned problem.
