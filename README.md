# Bloq--Screening-task

Methodology
The goal of this approach is to address credit risk modeling using a quantum-classifier that leverages Adiabatic Quantum Support Vector Classifier (AQSVC). Here’s a concise overview of the methodology:

Data Preprocessing:

We selected only the numerical attributes from the provided German Credit dataset, as they are well-suited for quantum optimization algorithms.
These features were standardized using StandardScaler to ensure consistency and improve the performance of the quantum solver.
Quantum Classifier (AQSVC):

We formulated the problem as a Quadratic Unconstrained Binary Optimization (QUBO) problem, which is the format required for quantum solvers.
The cost matrix was incorporated into the QUBO to prioritize the recall of the minority class (Bad credit), emphasizing penalties for misclassifying Bad credit customers as Good.
Quantum Solver:

The D-Wave quantum solver was used to solve the QUBO problem, exploring the solution space and optimizing the classification for the Bad credit class.
The best solution from the quantum solver was then mapped back to the predicted labels.
Evaluation:

The model's performance was evaluated using the recall score for the minority class (Bad credit), ensuring the classifier is focused on minimizing false negatives, which are critical in credit risk scenarios.
Original Ideas and Potential Applications
Bias towards Minority Class:

By utilizing a cost matrix to penalize misclassification of Bad credit customers more heavily than Good credit, this method ensures that the model has a high recall for the minority class. This is particularly crucial in credit risk, where identifying at-risk clients (Bad credit) is vital.
Quantum-classifier (AQSVC):

The use of quantum optimization via the D-Wave system represents a novel approach to credit risk modeling. Traditional methods might struggle with large-scale optimization and complex decision boundaries, but quantum algorithms like AQSVC can explore solution spaces more efficiently, potentially improving classification accuracy and robustness.
Applications:

This methodology is applicable in any domain requiring imbalanced classification where the minority class needs to be identified with high precision (e.g., fraud detection, medical diagnoses for rare diseases).
Specifically, in credit risk modeling, the approach can lead to better credit decision-making by ensuring that risky customers are correctly identified, minimizing potential financial losses.
By combining the cost-sensitive approach with quantum optimization, this methodology pushes the boundaries of traditional credit risk modeling, offering more effective and efficient ways to classify financial risk.
