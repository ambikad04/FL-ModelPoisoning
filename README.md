# Federated Learning with Model Poisoning

This project demonstrates a Federated Learning (FL) framework with the presence of a malicious client performing model poisoning. The simulation highlights the impact of poisoned updates on the global model's performance.

---

## Features

- **Federated Learning Workflow**: Simulates the entire FL process, including data generation, local training, and global aggregation.
- **Malicious Client Simulation**: Introduces poisoned updates into the FL system to analyze the effects on global model accuracy.
- **Synthetic Data Generation**: Creates client-specific datasets for training and testing.
- **Model Performance Evaluation**: Tests the global model's accuracy after FL training with poisoned updates.

---

## Installation

### Prerequisites
- Python 3.8+
- Required Libraries: PyTorch, NumPy

### Installation Steps
1. Clone the repository:
   ```bash
   git clone https://github.com/ambikad04/FL-ModelPoisoning.git 
   cd FL-ModelPoisoning
   ```

2. Install dependencies:
   ```bash
   pip install torch numpy
   ```

---

## Usage

1. Run the script:
   ```bash
   python FL_with_poisoning.py
   ```

2. Customize parameters:
   - Change the number of clients, global epochs, or the malicious client ID in the script for different scenarios.

---

## Code Structure

### Main Components:
1. **Data Generation (`create_client_data`)**:  
   Generates synthetic data for multiple clients.

2. **Model Definition (`SimpleModel`)**:  
   Defines a simple neural network for binary classification.

3. **Local Training (`train_local_model`)**:  
   Trains each client's model locally on their data.

4. **Malicious Behavior (`poison_model`)**:  
   Simulates a malicious client by introducing noise to model updates.

5. **Federated Learning (`federated_learning_with_poisoning`)**:  
   Manages the FL process, including global aggregation and malicious updates.

6. **Federated Averaging (`federated_averaging`)**:  
   Combines model updates from clients into a single global model.

---

## Example Output

When executed, the script logs the presence of a malicious client and completes the FL process. It also evaluates the global model's performance:

```
Client 1 is malicious in epoch 1.
Global epoch 1 completed.
Client 1 is malicious in epoch 2.
Global epoch 2 completed.
Client 1 is malicious in epoch 3.
Global epoch 3 completed.
Test Accuracy: 65.00%
```

---

## Results

The simulation demonstrates the impact of a malicious client on global model accuracy. You can adjust parameters like the scale of poisoning or the number of clients to observe different outcomes.

---


## Contributing

Contributions are welcome! Fork the repository, make your changes, and submit a pull request.

---

## Acknowledgments

This project is inspired by the Federated Learning paradigm and explores its challenges in adversarial scenarios.
```
