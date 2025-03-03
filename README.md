# Data-scientist-QA

## 1. Explain briefly batch gradient descent, stochastic gradient descent, and mini-batch gradient descent. and what are the pros and cons for each of them?

1. Batch Gradient Descent (BGD)
Definition: Uses the entire dataset to compute the gradient and update the model parameters in each iteration.
Pros:
More stable convergence (less noise in updates).
Efficient when dealing with small datasets.
Cons:
Computationally expensive for large datasets.
Slow updates since it processes the whole dataset before updating parameters.
2. Stochastic Gradient Descent (SGD)
Definition: Updates model parameters using only one randomly selected data point per iteration.
Pros:
Faster updates, allowing real-time learning.
Can escape local minima due to randomness.
Cons:
High variance in updates, leading to a noisier optimization process.
May not converge smoothly (fluctuations in loss function).
3. Mini-Batch Gradient Descent (MBGD)
Definition: Uses a small batch of data (e.g., 32 or 128 samples) to compute the gradient before updating parameters.
Pros:
A balance between BGD and SGD (faster than BGD, more stable than SGD).
Takes advantage of parallel computation.
Cons:
Still requires tuning batch size for optimal performance.
Slightly noisier than BGD but smoother than SGD.

| Method | Stability | Computation Cost | Convergence Speed | Best for |
|--------|------------|-----------------|------------------|----------|
| **BGD** | High (smooth updates) | High (entire dataset) | Slow | Small datasets |
| **SGD** | Low (noisy updates) | Low (single data point) | Fast | Online learning, large datasets |
| **MBGD** | Medium (less noisy than SGD) | Medium (mini-batches) | Faster than BGD, smoother than SGD | Large datasets, deep learning |

---

