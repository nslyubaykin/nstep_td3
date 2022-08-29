# Multi-Step Bootstrapping with [ReLAx](https://github.com/nslyubaykin/relax)

Example N-step TD3 [implementation](https://github.com/nslyubaykin/nstep_td3/blob/master/nstep_td3.ipynb) with [ReLAx](https://github.com/nslyubaykin/relax)

The performance versus vanilla 1-step TD is measured by averaging learning curves (for separate evaluation environment) over 4 experiments with random environment seeds.

The results are summarized in the following plot:

![n_step_vs_1_step](https://github.com/nslyubaykin/nstep_td3/blob/master/n_step_vs_1_step.png)

The only difference in hyper-parameters settings between N-step TD3 and vanilla TD3 is the presence of multi-step bootstrapping. 
We can see a substantial advantage of 3-step version in terms of training speed as well as asymptotic performance by looking at the averaged curves.
That shows that often N-step TD is the cheapest way of improving the performance of RL actor.
Note that from task to task the incremental performance of using N-step TD may vary. For example, early experiments show that for Mujoco's Ant-v2 environment 3-step Bellman update works worse than 1-step version.

__Resulting Policy__

https://user-images.githubusercontent.com/67604207/184318176-0759a7c2-079d-4896-8446-bd6b4016c248.mp4
