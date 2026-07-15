# Quantum Computing and Advanced Algorithms

Welcome to the **Design and Analysis of Algorithms (DAA) Project-Based Learning (PBL)** repository. This project explores the transition from advanced classical algorithm design to the paradigm-shifting domain of quantum computing, analyzing their architectures, implementations, and future implications.

---

## 📌 Project Overview
* **Course:** Design and Analysis of Algorithms (20CS22001)
* **Academic Year:** 2025-26 (II Year, II Semester)
* **Institution:** Geethanjali College of Engineering and Technology (Autonomous)
* **Department:** Computer Science and Engineering (Cyber Security) - Section A

### 👥 Batch 17 Members
* **P. Ileen Jasmine** (24R11A6231)
* **P. Pranitha** (24R11A6233)
* **R. Srivarsha** (24R11A6234)

**Under the Guidance of:** Ms. D. Subhashini

---

## 📝 Abstract
The rapid growth of computational demands in fields such as artificial intelligence, cryptography, and large-scale optimization has pushed traditional algorithm design to its limits. While advanced classical strategies continue to evolve, they face computational bottlenecks when handling exponential time complexities. 

This project explores the integration of advanced classical algorithms and quantum mechanics (superposition and entanglement). By analyzing frameworks, workflows, and algorithmic pseudocodes, this report sheds light on how hybrid computing environments will redefine the limits of future computational power.

---

## ⚙️ Algorithms Explored

### 1. Advanced Classical Algorithms
* **Divide and Conquer:** Breaks problems into smaller subproblems (e.g., Merge Sort) with a time complexity of $O(n \log n)$.
* **Dynamic Programming:** Eliminates redundant computations using memoization (e.g., Fibonacci, Knapsack Problem).
* **Greedy Algorithms:** Makes locally optimal choices at each stage (e.g., Dijkstra’s shortest path).
* **Parallel Algorithms:** Executes tasks simultaneously using multi-core processors and GPUs.
* **Machine Learning Algorithms:** Learns patterns from data for prediction, classification, and optimization.

### 2. Quantum Algorithms
* **Shor’s Algorithm:** Solves integer factorization in polynomial time ($O((\log n)^3)$), presenting a direct challenge to traditional RSA encryption.
* **Grover’s Algorithm:** Provides a quadratic speedup for searching unsorted datasets.
* **Quantum Fourier Transform (QFT):** Acts as a core building block for phase estimation and factoring.
* **Variational Quantum Algorithms (VQA):** Hybrid classical-quantum algorithms optimized for near-term quantum processors.

### 📊 Efficiency Comparison

| Problem | Classical Approach | Quantum Approach |
| :--- | :--- | :--- |
| **Search** | $O(n)$ | $O(\sqrt{n})$ |
| **Factorization** | Exponential | Polynomial |

---

## 💻 Implementation & Pseudocode

Quantum implementations are primarily explored using simulation frameworks like **Qiskit** (IBM) and **Cirq** (Google), while classical algorithms leverage structured languages like **C, C++, and Java**.

### Grover's Search Algorithm
```text
Algorithm GroverSearch(n, target)
// n: number of qubits, N = 2^n items
// target: index of target item (binary string)
// Returns: measured index with high probability

N ← 2^n                    // total search space size
r ← floor(π/4 * √N)        // optimal number of iterations
ψ ← uniform superposition   // |ψ⟩ = H^⊗n |0⟩^⊗n (1/√N amplitude each)

Repeat r times
    p2 ← oracle(ψ)          // apply oracle: flip phase of target state
    if (p2 ≠ next) then     
        p3 ← diffusion(p2)   // diffusion operator: 2|s⟩⟨s| - I
        if (||p3|| > 0) then ψ ← p3·next    
        else
            temp ← area(p2→ψ, p2→x)  
            if (temp > 0) then ψ ← (p3→y)·next
        end if
    end if
    prev ← ψ; ψ ← next        
End

Print measured_state(ψ)     // collapse to most probable state
End GroverSearch
