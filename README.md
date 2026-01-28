# step-by-step-derivation-for-the-covariance-matrix-calculation

#### 1. Notation and Dimensions
To eliminate ambiguity, we first clarify the dimensions of all variables used in the probabilistic framework:
* $J_s$: Total number of pixels in image $\mathcal{I}_s$ at scale $s$ (scalar).
* $x_j$: Spatial coordinates of the $j$-th pixel, where $x_j \in \mathbb{R}^2$.
* $H_i$: Ground-truth head position of the $i$-th person, where $H_i \in \mathbb{R}^2$.
* $\epsilon_i$: Annotation noise, assuming $\epsilon_i \sim \mathcal{N}(0, \alpha I)$, where $\epsilon_i \in \mathbb{R}^2, \alpha \in \mathbb{R}^+$.
* $\beta_s$: Variance of the Gaussian kernel at scale $s$ (scalar).
* $\mathbb{D}_s(x)$: Density random variable at pixel $x$ (scalar).
* $\mathbb{D}_s$: Density map vector for the entire scale, $\mathbb{D}_s = [\mathbb{D}_s(x_1), \dots, \mathbb{D}_s(x_{J_s})]^T \in \mathbb{R}^{J_s}$.
* $\mu_s$: Expected density map vector, $\mu_s \in \mathbb{R}^{J_s}$.
* $\Sigma_s$: Spatial Covariance Matrix, $\Sigma_s \in \mathbb{R}^{J_s \times J_s}$.
