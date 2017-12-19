# Fundamentals of Machine Learning

## Exercise 7

## 1 Proof - Ridge Regression - Primal vs Dual

For the primal version of ridge regression, the optimal $\hat\beta$ is given by
$$
\hat\beta = (X^TX + \tau \mathbb{I}_D)^{-1} X^T y
$$
while the optimal solution for the dual formulation of the problem is
$$
\hat\alpha = (XX^T+\tau\mathbb{I}_N)^{-1} y
$$
We now have to prove, that the optimal $\hat\beta$ corresponds to $\hat\alpha$:
$$
\hat\beta = X^T \hat\alpha
$$
First we proof the following lemma (1):
$$
(X^TX + \tau \mathbb{I}_D)^{-1} X^T = X^T  (XX^T+\tau\mathbb{I}_N)^{-1} \\
\Leftrightarrow X^T  (XX^T+\tau\mathbb{I}_N) = (X^TX + \tau \mathbb{I}_D) X^T
$$




We can prove this easily:
$$
X^T  (XX^T+\tau\mathbb{I}_N) = X^TXX^T + \tau X^T \mathbb{I}_N = X^TXX^T + \tau \mathbb{I}_N X^T = (X^TX+\tau \mathbb{I}_D) X^T
$$
Basic linear algebra shows $ \mathbb{I}_N X^T = X^T \mathbb{I}_D $
With that our lemma is proven.

Now we can prove relationship between $\hat\beta$ and $\hat\alpha$ (starting at optimal solution for $\beta$:
$$
\hat\beta = (X^TX + \tau \mathbb{I}_D)^{-1} X^T y  \overset{\text{lemma}}{=} X^T  (XX^T+\tau\mathbb{I}_N)^{-1} y = X^T \hat\alpha \qquad \square
$$












