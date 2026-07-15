# Quantum Computing and Advanced Algorithms

Welcome to the **Design and Analysis of Algorithms (DAA) Project-Based Learning (PBL)** repository. This project explores the transition from advanced classical algorithm design to the paradigm-shifting domain of quantum computing, analyzing their architectures, implementations, testing methodologies, and future implications.

---

## 📌 Project Overview

* **Course:** Design and Analysis of Algorithms - (20CS22001)
* **Academic Year:** A.Y 2025-26 (II Year, II Semester)
* **Institution:** Geethanjali College of Engineering and Technology (Autonomous)
* **Department:** Bachelor of Technology in Computer Science and Engineering (Cyber Security) - Section A

### 👥 Batch 17 Members

* **P. Ileen Jasmine** (24R11A6231)
* **P. Pranitha** (24R11A6233)
* **R. Srivarsha** (24R11A6234)

**Under the Guidance of:** Ms. D. Subhashini

---

## 📝 Abstract

The rapid growth of computational demands in fields such as artificial intelligence, cryptography, and large-scale optimization has pushed traditional algorithm design to its limits. Classical algorithms, though efficient for many problems, struggle with exponential complexity in certain domains.

Quantum computing introduces a transformative approach by utilizing principles such as superposition and entanglement, enabling new types of algorithms with potentially exponential speedups. This report explores the evolution of algorithm design, detailing classical advanced algorithms and quantum algorithms, their architecture, implementation strategies, testing methodologies, challenges, and future prospects.

---

## ⚙️ Algorithms Explored

### 1. Classical Advanced Algorithms

* **Divide and Conquer:** Breaks the problem into smaller subproblems (e.g., Merge Sort) with a time complexity of $O(n \log n)$.
* **Dynamic Programming:** Stores results of subproblems via memoization to reduce redundant calculations (e.g., Fibonacci, Knapsack Problem).
* **Greedy Algorithms:** Makes locally optimal choices (e.g., Dijkstra's shortest path).
* **Parallel Algorithms:** Executes tasks simultaneously utilizing multi-core processors and GPUs.
* **Machine Learning Algorithms:** Learns patterns from data for prediction, classification, and optimization.

### 2. Quantum Algorithms

* **Shor's Algorithm:** Solves integer factorization in polynomial time with a complexity of $O((\log n)^3)$, threatening RSA encryption.
* **Grover's Algorithm:** Searches an unsorted database efficiently, reducing complexity from $O(n)$ to $O(\sqrt{n})$.
* **Quantum Fourier Transform (QFT):** Acts as a core component in many quantum algorithms, used in phase estimation and factoring.
* **Variational Quantum Algorithms (VQA):** Hybrid classical-quantum algorithms used for optimization and machine learning.

### 📊 Efficiency Comparison

| Problem | Classical Approach | Quantum Approach |
| :--- | :--- | :--- |
| **Search** | $O(n)$ | $O(\sqrt{n})$ |
| **Factorization** | Exponential | Polynomial |

---

## 💻 Implementation & Pseudocode

Implementing advanced algorithms requires a structured approach, utilizing programming languages such as C, C++, and Java for classical models, and frameworks like Qiskit and Cirq for designing and simulating quantum circuits.

### Grover's Search Algorithm

```text
Algorithm GroverSearch(n, target)
/*
// n: number of qubits, N = 2^n items
// target: index of target item (binary string)
// Returns: measured index with high probability
*/

N ← 2^n                    // total search space size
r ← floor(π/4 * √N)        // optimal number of iterations
ψ ← uniform superposition   // |ψ⟩ = H^⊗n |0⟩^⊗n (1/√N amplitude each)

Repeat r times
    p2 ← oracle(ψ)          // apply oracle: flip phase of target state
    if (p2 ≠ next) then     // p2 marks target with phase flip
        p3 ← diffusion(p2)   // diffusion operator: 2|s⟩⟨s| - I
        /*
        // p3 reflects about average amplitude
        // amplifies target probability
        */
        if (||p3|| > 0) then ψ ← p3·next    // update state
        /*
        // move one iteration ahead
        */
        else
            temp ← area(p2→ψ, p2→x)  // compute reflection
            if (temp > 0) then ψ ← (p3→y)·next
            /*
            // if no target marked, continue
            */
        end if
    end if
    prev ← ψ; ψ ← next        // update pointers
End

Print measured_state(ψ)     // collapse to most probable state
End GroverSearch
```

### Convex Hull Algorithm

```text
Algorithm ConvexHull(pList)
/*
// pList is pointer to first node in input list
// Sort points according to angle made with p & x-axis
*/
Sort(pList)
Scan(pList)
PrintList(pList)
End ConvexHull
```

---

## 🛠️ Architecture and System Design

The architecture of modern computing systems plays a crucial role in algorithm design.

* **Classical Architecture:** Consists of CPUs, GPUs, memory systems, and distributed networks optimized for sequential or parallel execution.
* **Quantum Architecture:** Built around qubits that exploit superposition, entanglement, and interference via quantum gates and circuits. Physical systems like superconducting circuits or trapped ions are used to implement qubits.
* **Hybrid Systems:** Emerging frameworks combine classical and quantum computing, where classical computers handle general processing while quantum systems are leveraged for specialized tasks to achieve better performance.

---

## 🔬 Testing and Results

Testing ensures the correctness and efficiency of algorithms.

* **Classical Testing:** Evaluated using unit tests, integration tests, and performance benchmarks measuring execution time, memory usage, and scalability.
* **Quantum Testing:** More complex due to the probabilistic nature of quantum systems. Simulations are extensively used to validate results, while considering error rates and noise. Benchmarking against classical systems helps determine meaningful quantum advantages.

---

## ⚠️ Challenges Faced

* **Decoherence:** Quantum systems are highly sensitive to environmental disturbances, leading to errors and loss of information.
* **Qubit Limitations:** The number of available physical qubits is still limited, restricting the complexity of problems that can be solved.
* **Accessibility and Cost:** Quantum hardware remains expensive and is not widely accessible.
* **Steep Learning Curve:** Developing quantum algorithms requires specialized knowledge spanning both computer science and quantum physics.
* **Infrastructure Integration:** Integrating quantum systems with existing classical infrastructure presents additional technical challenges.

---

## 🔮 Future Scope

* **Hardware & Error Correction:** Focused research on developing more stable, scalable quantum systems and improving error correction techniques.
* **Hybrid Paradigms:** Increased adoption of hybrid algorithms combining classical and quantum approaches.
* **AI Integration:** Integrating artificial intelligence with algorithm design to produce more adaptive and efficient systems.
* **Cloud Quantum Computing:** Expanding cloud-based quantum platforms to make these technologies more accessible, enabling wider experimentation and development.

---

## 📚 References

1. Nielsen, M. A., & Chuang, I. L. – *Quantum Computation and Quantum Information*
2. Cormen, T. H. et al. – *Introduction to Algorithms*
3. IBM Quantum Documentation (Qiskit)
4. Google Quantum AI Research Publications
5. IEEE Xplore Digital Library
6. ACM Digital Library
