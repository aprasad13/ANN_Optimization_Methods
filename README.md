# Deep_Learning_Optimization_Methods

In this notebook, I have implemented some optimization methods that can speed up learning and perhaps even get us to a better final value for the cost function. Having a good optimization algorithm can be the difference between waiting days vs. just a few hours to get a good result.

### I have implemented following optimization algorithms:
- <Strong>Mini-Batch Gradient descent</strong>
- <Strong>Momentum</strong> (Momentum takes into account the past gradients to smooth out the update. Using momentum can reduce these oscillations)
- <Strong>Adam (Adaptive Moment Estimation)</strong> (Adam is one of the most effective optimization algorithms for training neural networks. It combines ideas from RMSProp (described in lecture) and Momentum)

I have used sklearn in-built "moons" dataset to test the above optimization methods.

Click to access the [Jupiter Notebook](https://github.com/aprasad13/Deep_Learning_Optimization_Methods/blob/master/Optimization_Methods.ipynb) for a detailed Code and Visualization.

### Performance

| optimization method  | train accuracy        | cost shape     | 
| ---------------------| --------------- | ---------------|
| Gradient descent     | 79.7%           | oscillations   | 
| Momentum             | 79.7%           | oscillations   | 
| Adam                 | 94%             | smoother       | 


Momentum usually helps, but given the small learning rate and the simplistic dataset, its impact is almost negligeable. Also, the huge oscillations you see in the cost come from the fact that some mini batches are more difficult thans others for the optimization algorithm.

Adam on the other hand, clearly outperforms mini-batch gradient descent and Momentum. If you run the model for more epochs on this simple dataset, all three methods will lead to very good results. However, you've seen that Adam converges a lot faster.

Some advantages of Adam include:
- Relatively low memory requirements (though higher than gradient descent and gradient descent with momentum) 
- Usually works well even with little tuning of hyperparameters (except $\alpha$)
