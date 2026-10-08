# First Neural Network

This repository contains a simple PyTorch-based neural network project created in Google Colab. The model learns to classify points in a 2D plane based on whether they fall inside or outside a circle.

## Project Goal

The notebook demonstrates a beginner-friendly neural network example:

- Generate random 2D points in the range [-1, 1]
- Label points based on whether they are inside a circle of radius 0.5
- Train a feedforward neural network using PyTorch
- Evaluate model accuracy
- Visualize the learned decision boundary
- Save the trained model weights

## What the model does

The network is a small binary classifier:

- Input layer: 2 features
- Hidden layer: 50 neurons with ReLU activation
- Output layer: 1 neuron with Sigmoid activation
- Loss function: Binary Cross Entropy (BCELoss)
- Optimizer: Adam

This is a classic example of learning a nonlinear decision boundary from synthetic data.

## Files in this repository

- `First_NN.ipynb` — the main Google Colab notebook containing all code and visualizations
- `README.md` — project overview and usage notes

## Open in Google Colab

You can open the notebook directly in Colab using the link below:

https://colab.research.google.com/github/iamMosab21/First__NN/blob/main/First_NN.ipynb

## Notebook workflow

The notebook includes the following steps:

1. Import PyTorch and Matplotlib
2. Create random 2D samples
3. Plot the raw data points
4. Define labels for points inside the circle
5. Build the neural network model
6. Train the model for 1000 epochs
7. Print training accuracy
8. Evaluate on test data
9. Plot the final decision boundary
10. Save the trained model as `circle_model.pth`

## Example training logic

```python
model = nn.Sequential(
    nn.Linear(2, 50),
    nn.ReLU(),
    nn.Linear(50, 1),
    nn.Sigmoid()
)

loss_function = nn.BCELoss()
optimizer = torch.optim.Adam(model.parameters(), lr=0.01)
```

## Dependencies

This project requires:

- Python 3
- PyTorch
- Matplotlib

Install dependencies with:

```bash
pip install torch matplotlib
```

## Example output

The notebook prints accuracy metrics like:

```python
Accuracy: 0.9990000128746033
Test accuracy: 0.9869999885559082
```

These values show that the neural network successfully learned the circular decision boundary.

## Project status

This is a simple introductory neural network project designed for learning and experimentation. It is a good starting point for understanding:

- feedforward networks
- binary classification
- loss functions
- model training in PyTorch
- data visualization with Matplotlib

## License

This project is provided for educational purposes.
