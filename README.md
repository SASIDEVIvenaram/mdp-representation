## POLICY EVALUATION
## AIM
To develop a Python program to evaluate the given policy.

## PROBLEM STATEMENT
To find best policy from two policies which are defined by user using policy evaluation function. Where the mdp includes 16 states from 0-15, 0 is the starting state, assigning some 4 random state as holes and 15 is the goal state and then we need to calculate optimal state value function for each state such that we can reach goal using optimal policy using policy evaluation.

## POLICY EVALUATION FUNCTION
def policy_evaluation(pi, P, gamma=1.0, theta=1e-10):
    prev_V = np.zeros(len(P), dtype=np.float64)
    # Write your code here to evaluate the given policy
    while True:
      V=np.zeros(len(P))
      for s in range(len(P)):
        for prob,next_state,reward,done in P[s][pi(s)]:
           V[s]+=prob*(reward+gamma *prev_V[next_state]*(not done))
      if np.max(np.abs(prev_V-V))<theta:
        break
      prev_V=V.copy()
    return V
## OUTPUT:
### First policy:


![image](https://github.com/user-attachments/assets/a78d9ed1-28b5-4eb9-98e6-e1a4d2bab9fe)

![image](https://github.com/user-attachments/assets/276977a3-80dd-410a-8d59-d8047c1958ce)


### Second policy:


![image](https://github.com/user-attachments/assets/b543c48e-635f-4560-8a09-557c9ec7de70)

![image](https://github.com/user-attachments/assets/4045ae9d-3798-4113-a77e-9cadcb66f2da)


### First and Second compared them:


![image](https://github.com/user-attachments/assets/ac18a0be-31cd-4538-8b99-ae7267a50103)


## RESULT:
Thus, The Python program to evaluate the given policy is successfully executed.
