# QAOA - MaxCut Problem

This project demonstrates how to solve the **Max-Cut problem** using the Quantum Approximate Optimization Algorithm (QAOA) with Qiskit and NetworkX.

## Overview

The Max-Cut problem is a classic combinatorial optimization problem: given a graph, partition its nodes into two sets such that the number of edges between the sets is maximized. QAOA is a hybrid quantum-classical algorithm that can efficiently approximate solutions to such problems.

## Steps in the Notebook

1. **Graph Construction**  
   A simple 4-node cycle graph is created using NetworkX.

2. **Hamiltonian Construction**  
   - **Mixer Hamiltonian ($H_m$):** Drives the quantum state towards superposition.
   - **Problem Hamiltonian ($H_p$):** Encodes the Max-Cut objective.

3. **QAOA Circuit Assembly**  
   - Initial state: All qubits in superposition.
   - Alternating application of mixer and problem Hamiltonians.

4. **Objective Function**  
   - Evaluates the quality of a bitstring solution for the Max-Cut.

5. **Expectation Calculation**  
   - Computes the expected value of the objective over all measured bitstrings.

6. **Parameter Optimization**  
   - Uses the COBYLA optimizer from SciPy to find optimal QAOA parameters.

7. **Results Visualization**  
   - Displays the probability distribution of bitstring solutions.
   - Highlights the best cuts found.

## Key Dependencies

- [Qiskit](https://qiskit.org/)
- [NetworkX](https://networkx.org/)
- [SciPy](https://scipy.org/)

## How to Run

1. Install dependencies:
    ```
    pip install qiskit networkx scipy matplotlib
    ```
2. Open `qaoa-maxcut.ipynb` in Jupyter or VS Code.
3. Run all cells to see the QAOA workflow and results.

## Results

The notebook finds that the bitstrings `0101` and `1010` are the most probable solutions, corresponding to the optimal Max-Cut for the given graph.

## References

- [Farhi et al., "A Quantum Approximate Optimization Algorithm"](https://arxiv.org/abs/1411.4028)
- [Qiskit Tutorials: QAOA](https://qiskit.org/documentation/tutorials/algorithms/07_qaoa.html)

---

*Explore quantum algorithms for