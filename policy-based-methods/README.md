# Policy based methods

RL is all about learning optimal policies from the interations with an environment. In value based methods we do

```python
Interation => optimal value function q* => optimal policy pi*
```

- Above optimal policy is built one state at a time by pulling values from the q table.
- When environment has much larger state space, e.g. cart pole balancing environment (cart position, cart velocity, pole angle, pole velocity at tip), table will be huge if we have a row for each state (which will render it unuseful in practice).
- A discretization technique has to be used here.
- In DQN, we represented optimal value function as a neural network. NN take environment takes environment state as an input and output the probability of each action value. In cart-pole the output will be if to move left or right the cart. We can get the best action by looking at the output NN produce for a given input state.
- In both the approaches (action table and DQN) we have to estimate optimal value function first to estimate the optimal policy. Can we directly find the optimal policy, without worrying about optimal value function?
- Yes, these can be achieved through policy based methods.

## Policy function approximation

