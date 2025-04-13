# 🧠 Quantum Portfolio Optimization with HHL++

This project showcases an enhanced quantum algorithm (HHL++) tailored for solving Linear Systems in the context of Portfolio Optimization. It combines traditional quantum techniques like Quantum Phase Estimation (QPE) with novel enhancements such as hybrid eigenvalue inversion and fidelity benchmarking.

---

## 🚀 Key Features

- **HHL++ Engine**: Modified HHL with improved inversion logic and preprocessing pipeline.
- **PortfolioQLSP**: Encodes portfolio optimization as a Quantum Linear System Problem.
- **Preprocessing Module**: Data is transformed using classical techniques to make it quantum-friendly.
- **Dynamic Fidelity Reporting**: Quantitative measure of how closely our quantum solution matches the classical benchmark.
- **Visualizations**: Plots that compare classical vs quantum amplitudes and illustrate measurement distributions.
- **Benchmarking**: Compare HHL++ with basic HHL and brute-force inversion for both performance and fidelity.

---

## Project Structure

```bash
📦 quantum-portfolio-hhlpp/
├── hhlpp_final_verified_no_assemble.ipynb  # Main notebook with HHL++ implementation
├── README.md                               # This file
├── 📊 Visuals                              # Dynamically generated plots and performance graphs
```

---

## Use Case

Quantum computers are uniquely suited to solve certain linear algebra problems exponentially faster. Portfolio Optimization—finding the best asset allocation to maximize return and minimize risk—can be reframed as solving a system Ax = b, where:

- **A**: Covariance matrix of assets (risk model)
- **b**: Encodes constraints, expected return, and budget

By encoding this into a quantum linear system and using HHL++, we:

- Reduce time complexity
- Enable high-speed decisions for high-frequency financial strategies
- Maintain or improve accuracy through our preprocessing and enhanced inversion

---

## How to Use This Project

1. **Clone or Download the Project**
```bash
git clone https://github.com/yourusername/quantum-portfolio-hhlpp.git
cd quantum-portfolio-hhlpp
```

2. **Install Dependencies**
You will need Python ≥ 3.9 and the following packages:
```bash
pip install qiskit matplotlib numpy scipy
```

3. **Run the Notebook**
Open `hhlpp_final_verified_no_assemble.ipynb` in JupyterLab, Jupyter Notebook, or Google Colab. Make sure to:
- Run all cells sequentially
- Use `Shift+Enter` to step through each part
- View outputs inline (includes fidelity, circuit depth, measurement counts, and plots)

4. **Compare Performance**
Check out:
- Fidelity score (closeness to classical)
- Depth of circuit (indicates quantum resource usage)
- Visual comparison between classical and quantum amplitudes

---

## Output Example

```
✅ Fidelity: 0.82
🔄 Circuit depth: 12
📊 Measurement counts: {'1 0001': 311, '0 0111': 345, ...}
```

---

## Why Our Method is Better

| Method           | Fidelity ↑ | Depth ↓ | Runtime ↓ | Qubit Use |
|------------------|------------|---------|------------|------------|
| **HHL++ (ours)** | ✅ High     | ✅ Low  | ✅ Fast    | Moderate   |
| Vanilla HHL      | Medium     | High    | Slow       | High       |
| Classical Solver | Exact      | N/A     | Slow       | None       |

- We preprocess A and b for better conditioning
- Use hybrid inversion for numerical stability
- Fidelity computation isolates signal from noise (only ancilla = 1)

---

## References

- Harrow, Hassidim, and Lloyd (2009). *Quantum Algorithm for Linear Systems of Equations.*
- Qiskit Documentation (v2.0 Migration Guide)
- Applications in Quantum Finance & Optimization

---

## Contributing

If you’re passionate about quantum finance or HHL variants, feel free to:
- Fork the repo
- Make changes or enhancements
- Submit a pull request

---

## Final Note

This notebook is more than just a demonstration. It is a testbed for high-performance quantum finance models. By combining domain-specific encoding, adaptive inversion, and high-fidelity validation, HHL++ shows how quantum technology can redefine optimization.

“Solve faster, solve better. Quantumly.”
