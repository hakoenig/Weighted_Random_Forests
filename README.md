# Weighted_Random_Forests
Experiments to improve Random Forests by weighting Trees according to their performance.

I was wondering if we could improve the accuracy of Random Forests by giving more weights to the trees that achieve a better performance on the training set.

I did two experiments.
In the first experiment, (*Random_Forest_Adjusted_Weights.ipynb*), weights are assigned to each tree according to the tree's accuracy on the whole training set.
In the second experiment, (*Random_Forest_Adjusted_Weights_TopK.ipynb*), weights are assigned to each tree according to the tree's out-of-bag accuracy. I also considered precision at the 1, 5, 10, 25% as the metric to evaluate the experiment on.

Unfortunately, in both cases, the weighted Random Forest did not improve precision or accuracy consistently.

For the next iteration, I am considering assigning weights based on a tree's precision at k on the OOB samples.
