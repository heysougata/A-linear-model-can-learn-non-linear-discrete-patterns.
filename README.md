# A-linear-model-can-learn-non-linear-discrete-patterns.
Here's how:

During model development, one of the techniques that many don’t experiment with is feature discretization.

The core idea is to transform a continuous feature into discrete features, mostly one-hot encoded.

𝐖𝐡𝐲 𝐰𝐨𝐮𝐥𝐝 𝐰𝐞 𝐝𝐨 𝐭𝐡𝐚𝐭?

My rationale for using feature discretization has almost always been simple: “It just makes sense to discretize a feature.”

For instance, consider a transactional dataset that has an age feature.

We wish to understand the spending behavior of users.

In such cases, continuous features like age are better understood when they are discretized into meaningful groups → youngsters, adults, and seniors.

Modeling this dataset without discretization will result in some coefficients for each feature.

They would tell us the influence of each feature on the final prediction.

But if you think again, in our goal of understanding spending behavior, are we really interested in learning the correlation between exact age and spending behavior?

It makes very little sense to do that.

Instead, it makes more sense to learn the correlation between different age groups and spending behavior.

Thus, discretizing the age feature can unveil much more valuable insights.

--

𝐀𝐝𝐯𝐚𝐧𝐭𝐚𝐠𝐞𝐬

In fact, one advantage of feature discretization is that it enables non-linear behavior in a linear model.

This can potentially lead to better accuracy, which is also evident from the image below.

A linear model with feature discretization results in a:
- non-linear decision boundary.
- better test accuracy.

So, in a way, we use a simple linear model but still get to learn non-linear patterns.

Another advantage is that it helps us improve the signal-to-noise ratio. Binnng a feature mitigates the influence of minor fluctuations, which are often noise.

--

𝐂𝐚𝐮𝐭𝐢𝐨𝐧𝐚𝐫𝐲 𝐦𝐞𝐚𝐬𝐮𝐫𝐞𝐬

Feature discretization with one-hot encoding increases the data dimensionality.

And typically, as we progress towards higher dimensions, data become more easily linearly separable.

Thus, feature discretization can lead to overfitting.

To avoid this, DON'T overly discretize your features.

Instead, use it when it makes intuitive sense, as we saw above.

Of course, its utility can vastly vary from one application to another, but I have found that:
- Discretizing geospatial data like latitude and longitude can be useful.
- Features that are typically constrained between a range, like age/weight-related data can be useful.
  
![Information](https://github.com/user-attachments/assets/4d2ed015-5948-4804-b03d-07b2071c633b)
