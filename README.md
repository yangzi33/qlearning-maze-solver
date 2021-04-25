# Maze Solver using Reinforcement Learning

We implemented a simulated environment and build a reinforcement learning agent that discovers the optimal (shortest) path to a goal. The agent’s environment will look like:

<img src="https://github.com/yangzi33/rl-maze-solver/blob/main/maze.png?raw=true" width="500" height="500" />

Each cell is a state in the environment. The cell labeled “I” is the initial state of the agent. The cell labeled “G” is the goal state of the agent. The black cells are barriers—states that are inaccessible to the agent. At each time step, the agent may move one cell to the left, right, up, or down. The environment does not wraparound. Thus, if the agent is in the lower left corner and tries to move down, it will remain in the same cell. Likewise, if the agent is in the initial state and tries to move up (into a barrier), it will remain in the same cell.

We Implement a Q learning algorithm that selects moves for the agent. The algorithm should perform exploration by choosing the action with the maximum Q value 90% of the time, and choosing one of the four actions at random the remaining 10% of the time. We should ”break-ties” when the Q-values are zero for all the actions (happens initially) by essentially choosing uniformly from the action. So now you have two conditions to act randomly: for $\epsilon$ amount of the time, or if the Q values are all zero.

The simulation consists of a series of trials, each of which runs until the agent reaches the goal state, or until it reaches a maximum number of steps, which you can set to 100. The reward at the goal is 10, but at every other state is 0. You can set the parameter $\gamma$ to 0.9.

Check `rl_maze_solver.py` for more details on experiments.


