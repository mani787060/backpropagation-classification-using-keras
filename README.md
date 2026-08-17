# 🧠 Backpropagation Classification Using Keras

## 📌 Project Overview

This project demonstrates how to solve a **binary classification problem using an Artificial Neural Network (ANN)** trained with backpropagation through **Keras with TensorFlow** as the backend.

The project builds on the concepts explored in the **Backpropagation Classification From Scratch** project and shows how the same fundamental learning process can be implemented efficiently using a modern Deep Learning framework.

Instead of manually calculating gradients and updating weights, Keras handles the underlying backpropagation and optimization process automatically.

---

## 🎯 Objective

The objective is to build a neural network that predicts whether a student is **placed or not placed** based on:

* CGPA
* Profile Score

### Target Variable

```text
placed
```

Where:

```text
1 → Placed
0 → Not Placed
```

This makes the project a **binary classification problem**.

---

## Dataset

A small dataset is created using Pandas:

```python
pd.DataFrame(
    [
        [8, 8, 1],
        [7, 9, 1],
        [6, 10, 0],
        [5, 5, 0]
    ],
    columns=['cgpa', 'profile_score', 'placed']
)
```

### Features

| Feature         | Description                |
| --------------- | -------------------------- |
| `cgpa`          | Academic performance score |
| `profile_score` | Candidate profile score    |

### Target

| Target   | Description              |
| -------- | ------------------------ |
| `placed` | Binary placement outcome |

---

## Neural Network Approach

The project uses a **Feedforward Artificial Neural Network**.

The general workflow is:

```text
Input Features
      ↓
Dense Layer
      ↓
Activation Function
      ↓
Output Layer
      ↓
Sigmoid Probability
      ↓
Predicted Class
```

The network learns the relationship between the candidate's features and placement outcome through repeated training iterations.

---

## Project Workflow

The notebook follows a complete Deep Learning classification workflow:

1. Create and inspect the dataset
2. Separate features and target
3. Prepare the input data
4. Define the neural network architecture
5. Configure the model
6. Select the loss function
7. Select the optimizer
8. Train the model
9. Generate predictions
10. Convert probabilities into class labels
11. Evaluate the model

---

## Backpropagation with Keras

During training, Keras automatically performs the major steps involved in neural network learning:

```text
Forward Propagation
        ↓
Prediction
        ↓
Loss Calculation
        ↓
Backpropagation
        ↓
Gradient Calculation
        ↓
Weight Update
        ↓
Repeat
```

The framework handles these calculations internally, allowing the developer to focus on designing, training, and evaluating the neural network.

---

## Activation Function

For binary classification, the output layer uses the **Sigmoid activation function**.

It produces a value between `0` and `1`, which can be interpreted as the probability of the positive class.

The predicted probability can then be converted into a class:

```text
Probability ≥ 0.5 → 1 (Placed)
Probability < 0.5 → 0 (Not Placed)
```

---

## Loss Function

The model uses a binary classification loss function to measure the difference between the predicted probability and the actual target.

The loss provides the signal required by backpropagation to update the network's weights during training.

---

## Optimizer

An optimizer is responsible for updating the neural network's parameters based on the calculated gradients.

This project demonstrates how Keras can handle the optimization process without manually implementing gradient calculations.

Depending on the notebook configuration, optimizers such as **Gradient Descent or Adam** can be used.

---

## Model Evaluation

The model can be evaluated using classification metrics such as:

* Accuracy
* Confusion Matrix
* Precision
* Recall
* Classification Report

For a small educational dataset, these metrics help understand how the model's predictions compare with the actual placement outcomes.

---

## From-Scratch vs Keras Implementation

This project is particularly useful when viewed alongside the **Backpropagation Classification From Scratch** project.

| From Scratch                        | Keras                             |
| ----------------------------------- | --------------------------------- |
| Manual forward propagation          | Framework handles it              |
| Manual loss calculation             | Built-in loss functions           |
| Manual gradient calculation         | Automatic differentiation         |
| Manual weight updates               | Optimizer handles updates         |
| Focus on mathematical understanding | Focus on practical implementation |
| More code                           | Concise and scalable              |

The comparison demonstrates how modern Deep Learning frameworks abstract complex mathematical operations while still relying on the same fundamental concepts.

---

## Key Concepts Demonstrated

* Artificial Neural Networks
* Binary Classification
* Forward Propagation
* Backpropagation
* Automatic Differentiation
* Activation Functions
* Sigmoid Function
* Binary Classification Loss
* Gradient Descent
* Adam Optimizer
* Model Training
* Model Evaluation

---

## Technologies Used

* **Python**
* **NumPy**
* **Pandas**
* **TensorFlow**
* **Keras**
* **Scikit-learn** (for evaluation, where applicable)

---

## Project Structure

```text
backpropagation-classification-using-keras/
│
├── backpropagation-classification-using-keras.ipynb
└── README.md
```

---

## Learning Outcomes

Through this project, I gained practical experience in:

* Building neural networks using Keras
* Configuring binary classification models
* Understanding how Keras performs backpropagation
* Using activation and loss functions
* Working with optimizers
* Training neural networks
* Generating classification predictions
* Evaluating model performance
* Connecting theoretical concepts with practical Deep Learning frameworks

---

## Future Improvements

Possible extensions include:

* Train the model on a larger real-world dataset
* Add more hidden layers
* Experiment with different activation functions
* Compare SGD and Adam optimizers
* Tune learning rate and batch size
* Add Dropout regularization
* Implement Early Stopping
* Visualize training and validation loss
* Visualize the decision boundary
* Compare the Keras implementation with the from-scratch implementation
* Deploy the trained model as an interactive application

---

## Final Takeaway

This project demonstrates how the theoretical concepts of **backpropagation and gradient-based learning** can be translated into a practical neural network using Keras.

The key learning is that although Keras hides the mathematical complexity behind automatic differentiation and optimizers, the underlying learning process remains the same:

**Prediction → Loss → Gradients → Weight Updates → Learning**

This project therefore serves as a bridge between **understanding neural networks from first principles** and **building practical Deep Learning models using modern frameworks**.
