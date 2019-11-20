# Policy Gradients
This repo is a TensorFlow implementation of the policy gradients assignment from Dr. Sergey Levine's CS 294-112 
Deep Reinforcement Learning. The code to run the experiments for this project can be found in the repo along with 
the code to plot and log the results. The code to plot and log the results along with the initial starter code were 
provided with the assighment. Videos of some of the trained agents as well as the results for each experiment are shown and discussed
below:

# Videos

<img src="/Videos/cartpole.gif" height="300px" width="300px" > | <img src="/Videos/lunar_lander.gif" height="300px" width="300px">

# CartPole

Experiments were run in the cartpole environment examining the impact of batch size, using reward-to-go, and normalizing the advantages. The following plot shows the impact of each where dna corresponds to unnormalized advantages, lb vs. sb corresponds to large batch vs. small batch sizes, and rtg signifies if reward to go was used. It can be seen in the plots that batch size and using reward-to-go had the most significant impact on performance, while normalizing the advantages did not have much of an effect:

![figure 1](https://raw.github.com/JackBrady/Policy_Gradients/master/Plots/small_batch_cart_pole.png)

![figure 2](https://raw.github.com/JackBrady/Policy_Gradients/master/Plots/large_batch_cart_pole.png)

# InvertedPendulum

Experiments were run in the inverted pendulum environment with the goal of finding the smallest possible parameters for batch size and learning rate which achieved a maximum score of 1000 in less than 100 iterations. The parameters that were found were a learning rate of 0.007 and a batch size of 2500. The plot for the experiment can be seen below:

![figure 1](https://raw.github.com/JackBrady/Policy_Gradients/master/Plots/inverted_pend.png)

The following experiments were run after implementing a state-dependent baseline via a neural network

# LunarLander

This experiment was run in the lunar lander environment utilizing the neural network baseline. A batch size of 40000 and a learning rate of 0.005 were used. The plot for the experiment can be seen below:

![figure 1](https://raw.github.com/JackBrady/Policy_Gradients/master/Plots/lunar_lander.png)

# HalfCheetah

These experiments examined the impact of reward-to-go and a neural network baseline in the HalfCheetah environment. A batch size of 30000 with a learning rate of 0.02 were found to be appropriate values as larger batch sizes along with a larger learning rate were empirically found to boost performance. It can be seen below that using reward-to-go as well as the neural network baseline gave superior results:

![figure 1](https://raw.github.com/JackBrady/Policy_Gradients/master/Plots/cheetah_plot.png)






