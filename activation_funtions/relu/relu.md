### 🔹 What is the ReLU Function?

The **Rectified Linear Unit (ReLU)** is one of the most widely used activation functions in modern neural networks. It outputs the input directly if it is positive; otherwise, it outputs zero. This simplicity makes it computationally efficient and effective for deep networks.

---

### 🔹 Formula

$$
\text{ReLU}(x) = \max(0, x)
$$

Where:  
- \( x \) is the input to the function  
- \( \max(0, x) \) returns 0 if \( x \leq 0 \), otherwise it returns \( x \)

---

### 🔹 Graph

The ReLU function is a **piecewise linear** function:

- When \( x < 0 \), \( \text{ReLU}(x) = 0 \)  
- When \( x \geq 0 \), \( \text{ReLU}(x) = x \)

This creates a function that is **flat for negative values** and **linear for positive values**.

---

### 🔹 Example Outputs

| Input (x) | Output (ReLU(x)) |
|-----------|------------------|
| -3        | 0                |
| -1        | 0                |
|  0        | 0                |
|  1        | 1                |
|  3        | 3                |

---

### 🔹 Why use ReLU?

- **Efficient computation**: Simple max operation  
- **Sparse activation**: Outputs 0 for half the input space, encouraging sparsity  
- **Mitigates vanishing gradient**: Unlike sigmoid/tanh, gradients do not shrink for positive inputs  
- **Works well in practice**: Especially in deep neural networks

---

### 🔹 Drawbacks

- **Dying ReLU Problem**: Neurons can "die" during training, getting stuck in the zero output region and never activating again (especially with high learning rates)  
- **Not zero-centered**: May lead to slower convergence compared to tanh

---

### 🔹 Derivative (Used in Backpropagation)

$$
\frac{d}{dx}[\text{ReLU}(x)] = 
\begin{cases}
0 & \text{if } x < 0 \\
1 & \text{if } x > 0 \\
\text{undefined} & \text{if } x = 0
\end{cases}
$$

In practice, the derivative at \( x = 0 \) is usually set to either 0 or 1 arbitrarily.

---

### 🔹 When to Use

Use **ReLU** in most hidden layers of deep neural networks. It is the default choice due to its simplicity and performance benefits. However, consider variants like **Leaky ReLU** or **ELU** if the dying neuron problem occurs.
