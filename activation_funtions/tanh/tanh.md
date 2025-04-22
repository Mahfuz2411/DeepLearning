### 🔹 What is the Tanh Function?

The Hyperbolic Tangent (Tanh) function is another commonly used activation function in neural networks. It maps any real-valued input to a value between -1 and 1. It’s a scaled and shifted version of the sigmoid function.

Unlike sigmoid, tanh is **zero-centered**, which often helps optimization during training.

---

### 🔹 Formula

$$
\tanh(x) = \frac{e^x - e^{-x}}{e^x + e^{-x}}
$$

Where:
- \( x \) is the input to the function  
- \( e \) is Euler’s number (approx 2.718)

---



### 🔹 Graph

The Tanh function has an "S"-shaped curve, similar to Sigmoid, but it ranges between -1 and 1.

- When \( x \to -\infty \), \( \tanh(x) \to -1 \)
- When \( x = 0 \), \( \tanh(x) = 0 \)
- When \( x \to +\infty \), \( \tanh(x) \to 1 \)

This zero-centered curve helps with optimization, especially when the data has both negative and positive values.

---

### 🔹 Example Outputs

| Input (x) | Output (tanh(x)) |
|-----------|------------------|
| -3        | ≈ -0.995         |
| -1        | ≈ -0.761         |
|  0        | 0                |
|  1        | ≈ 0.761          |
|  3        | ≈ 0.995          |

---

### 🔹 Why use Tanh?

- Output between -1 and 1 → zero-centered, which helps gradient descent converge faster  
- Smooth and differentiable  
- Strong gradients in the central region around 0

---

### 🔹 Drawbacks

- Vanishing Gradient Problem: Like sigmoid, for very large or small values of \( x \), the gradient becomes very small  
- Saturates at the ends (near -1 and 1), which can slow down learning

---

### 🔹 Derivative (Used in Backpropagation)

$$
\frac{d}{dx}[\tanh(x)] = 1 - \tanh^2(x)
$$

---

### 🔹 When to Use

Use **Tanh** when your inputs can be both positive and negative and you want a zero-centered activation function. Commonly used in hidden layers of neural networks.
