# ⚙️📈 ADAPTIVE vs STANDARD LEARNING RATE — MAIN QUEST

> *“Control the pace. Stabilize the climb. Converge smarter.”*

---

## 🗺️ Quest Overview

Training Machine Learning models is not just about *reaching* the objective — it’s about **how efficiently you get there**.

This project explores and compares two training strategies:

* ⚔️ **Standard Learning Rate** — fixed, predictable, reliable
* 🧠 **Adaptive Learning Rate** — dynamic, responsive, but volatile

The goal of this quest is to **analyze convergence behaviour, stability, and performance trade-offs** between these two approaches using controlled experiments and evaluation metrics.

---

## 📁 Quest Inventory (Project Structure)

```
.
├── AIII_Assignement2_u19258349.ipynb   # Main quest logic & experiments
├── README.md                          # Quest log
```

---

## ⚙️ Tech Stack — Gear Equipped

* **Python 3**
* **NumPy** — numerical spellcasting
* **Pandas** — data wrangling
* **Matplotlib / Seaborn** — visual scouting tools
* **Scikit-learn** — metrics & evaluation

---

## 🧠 Training Strategy — Skill Paths

### ⚔️ Standard Learning Rate Path

* Uses a **fixed learning rate** throughout training
* Simple, stable, and predictable
* Serves as the **baseline build**

---

### 🧠 Adaptive Learning Rate Path

* Learning rate adjusts dynamically during training
* Intended to:

  * Speed up convergence
  * Respond to loss behaviour
* Current implementation adapts based on **recent step behaviour**

---

## 📊 Evaluation Arena — Battle Metrics

Models are evaluated using:

* **Loss curves** during training
* **Accuracy / performance metrics**
* **Confusion matrices** for prediction quality

Lower loss and clearer class separation indicate a stronger build.

---

## 🏁 Quest Results

* Adaptive LR shows potential for faster convergence
* Standard LR offers more stable and predictable training
* Performance differences are observable but require stronger visual analysis

This sets the stage for future optimization.

---

## 🚧 Known Weaknesses & Future Upgrades (Side Quests)

The current build completes the main quest, but several **side quests** remain to strengthen the system.

---

### 🧩 Side Quest 1: Sentinel Value Handling (`-9999`)

**Current Weakness:**

* Sentinel values such as `-9999` are not explicitly handled
* They may be silently dropped or distort statistics

**Upgrade Path:**

* Explicitly convert sentinel values to `NaN` *before* cleaning

```python
df.replace(-9999, np.nan, inplace=True)
df.dropna(inplace=True)
```

This ensures data integrity and transparent preprocessing.

---

### 📈 Side Quest 2: Visual Comparison of LR Builds

**Current Weakness:**

* Adaptive vs Standard LR comparison is mostly numerical
* Behavioural differences are harder to interpret

**Upgrade Path:**

* Add comprehensive visualizations:

  * Loss curves (side-by-side)
  * Accuracy trends
  * Convergence speed plots
* Use the provided **comparison helper functions** consistently

Visual scouting dramatically improves insight into training dynamics.

---

### 🧠 Side Quest 3: Adaptive Learning Rate Stability

**Current Weakness:**

* Adaptive LR relies on a **single previous step**
* Highly sensitive to noise and short-term fluctuations

**Upgrade Path:**

* Replace with a smoother adaptation strategy:

  * **Fixed sliding window average**, or
  * **Exponential Moving Average (EMA)** over recent steps

This reduces volatility and improves convergence reliability.

---

### 🔥 Side Quest 4: Confusion Matrix Visualization

**Current Weakness:**

* Confusion matrices are printed as text
* Hard to visually inspect class-wise performance

**Upgrade Path:**

* Replace text output with **heatmap visualizations**

```python
sns.heatmap(cm, annot=True, fmt='d', cmap='Blues')
```

Heatmaps make strengths and weaknesses immediately visible.

---

## ✅ Quest Completion Summary

🧩 **Main Quest:** Learning Rate Strategy Comparison
🎯 **Objective:** Understand convergence and stability trade-offs
🚀 **Outcome:** Functional comparison with clear upgrade paths

With improved preprocessing, stronger adaptive logic, and richer visualizations, this project can evolve from an academic prototype into a polished experimental framework.

---

## 👤 Player Profile

**Wadalisa Oratile Molokwe**
Honours Student | Network Engineer & System Administrator

---

*Honours-level project — tuned for insight, not brute force.*
