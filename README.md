# Minesweeper-AI
# 💣 Minesweeper AI: CSP vs Probabilistic Reasoning

## 📌 Overview

This project implements an intelligent agent to solve the Minesweeper game using **two independent AI approaches**:

* Constraint Satisfaction Problem (CSP)
* Probabilistic reasoning (exact inference + Monte Carlo)

The goal is not only to solve the game, but to **compare deterministic vs uncertainty-based decision making in AI systems**.

---

## 🧠 AI Approaches

### 1. CSP-based Agent

* Knowledge-based reasoning
* Logical inference using constraints (sentences)
* Identifies safe cells and mines with certainty

✔ Strength:

* Guaranteed correctness when inference is possible

❌ Limitation:

* Fails when uncertainty appears (no safe moves)

---

### 2. Probabilistic Agent

* Builds constraint models from the board
* Uses:

  * Exact inference (backtracking)
  * Monte Carlo sampling (for large states)
* Computes probability of each cell being a mine

✔ Strength:

* Can act under uncertainty

❌ Limitation:

* Slower and not always optimal

---

## ⚖️ Comparison

| Feature             | CSP                  | Probabilistic |
| ------------------- | -------------------- | ------------- |
| Deterministic       | ✅                    | ❌             |
| Handles uncertainty | ❌                    | ✅             |
| Speed               | Fast                 | Slower        |
| Accuracy            | High (when solvable) | Risk-based    |

---

## 🏗️ System Architecture

```
Game Engine (Minesweeper)
        ↓
AI Agent
 ├── CSP Reasoning
 └── Probabilistic Inference
        ↓
Decision Making
```

---

## 🎮 Features

* Playable Minesweeper (Pygame)
* AI autoplay mode
* Safe vs mine visualization
* Performance stats (win rate, speed)
* Two independent AI agents

---

## ▶️ Installation & Run

### Install dependencies

```bash
pip install pygame
```

### Run CSP agent

```bash
python game/runner_csp.py
```

### Run Probabilistic agent

```bash
python game/runner_probabilistic.py
```

---

## 📊 Example Behavior

* CSP:

  * Plays perfectly when logic is sufficient
  * Stops when no safe move is known

* Probabilistic:

  * Chooses lowest-risk move
  * Continues even under uncertainty

---

## ⚠️ Limitations

* No learning (non-adaptive)
* Performance drops on large boards
* Probabilistic agent depends on sampling

---

## 🚀 Future Improvements

* Hybrid AI (CSP + Probability)
* Reinforcement Learning agent
* Performance benchmarking system
* Visualization dashboard

---

## 🧠 Key Takeaways

* Difference between symbolic AI and probabilistic AI
* Trade-offs between certainty and risk
* Constraint modeling and inference techniques

---

## 📸 Demo

-CSP
<img width="800" height="469" alt="CSP" src="https://github.com/user-attachments/assets/3d9038c4-9669-4419-b0a4-8e81f8da6fd1" />

-Probability model
<img width="800" height="469" alt="PM" src="https://github.com/user-attachments/assets/4db4495e-057e-4706-a21f-fc317719f35d" />

---

## 👨‍💻 Author

Pham Tan Minh

---

## 📄 License

This project is licensed under the MIT License.
