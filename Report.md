# Report

## Learning algorithm
The agent was trained using DDPG. DDPG uses two networks:  

- the actor approximates the optimal policy deterministically.
- the critic learns to evaluate the optimal action value function with actor's best believed action.

In DQN, you have two copies of the network (regular and target) and target network is updated every N steps.  

## Hyperparameters
The following hyperparameters were used:  

- buffer size: 1e5  
- minibatch size: 256  
- gamma: 0.995  
- tau: 3e-1  
- learning rate: 1e-3  
- beta: 1.0  

### Neural networks

#### The actor network:
- Batch normalization  
- Input layer: the state size  
- 1st hidden layer: 128 neurons (relu)  
- 2nd hidden layer: 128 neurons (relu)  
- output layer: 2 neurons (1 for each action) (tanh)  

### The critic network:
- Batch normalization  
- Input layer: the state size  
- 1st hidden layer: 128 neurons (relu)  
- 2nd hidden layer: 128 neurons (relu)  
- output layer: 1 neuron  

## Plot of Rewards
The agent was able to solve the environment after 866 episodes achieving an average maximum score of 0.50 over the last 100 episodes of the training process.

The average maximum scores of the 2 agents during the training process:  
![image](https://user-images.githubusercontent.com/65574771/212697531-f9475b5a-6cae-4d8c-9d38-120d7db26d82.png)


## Ideas for future work
For the future id defenitaly would like to experment more with different hyperparameter values. I'd also would like to implement an environment where the user can play against the agent.
