# TOC_NFA-to-DFA_converter
# NFA → DFA Converter with Minimization

An interactive web application that simulates the complete
Theory of Computation pipeline:
**NFA → DFA (Subset Construction) → Minimized DFA (Hopcroft's Algorithm)**

Built as a Class Participation project for the
Theory of Computation course — IIIT Sri City.

---

## 🔗 Live Demo

[Click here to open the simulation](https://toc-nfa-to-dfa-converter-pe84.vercel.app/)

---

## 📌 Topic

**Module 2 — Finite Automata**
- NFA to DFA Conversion (Subset Construction Algorithm)
- DFA Minimization (Partition Refinement / Hopcroft's Algorithm)

---

## 📖 What This Simulates

### 1. NFA Input
- Define states, alphabet, start state, and final states
- Fill the transition table (supports multiple targets and ε transitions)
- Live ε-closure preview for every state

### 2. NFA → DFA (Subset Construction)
- Computes ε-closure of the start state
- Iteratively applies move() and ε-closure() for each symbol
- Discovers new DFA states step by step
- Supports step-by-step mode and auto-run with speed control

### 3. DFA Minimization (Hopcroft's Algorithm)
- Splits states into final and non-final groups
- Refines partitions by distinguishability
- Merges equivalent states into one
- Shows every partition iteration (INIT → ITER → STABLE)
- Displays the minimized DFA transition table

### 4. Graph Visualization
- Live directed graph for NFA, DFA, and Minimized DFA
- Separate curved arrows for bidirectional transitions
- Self-loop arrows drawn like standard automata diagrams
- Highlighted active state and edge during step-by-step

### 5. String Simulator
- Input any string and simulate it on the DFA
- Step-by-step or auto mode
- Shows ACCEPTED / REJECTED with full path explanation

---

## ⚙️ How to Use

1. Enter states, alphabet, start state, final states
2. Click **Build Transition Table**
3. Fill in the transitions
4. Click **▶ Convert** to run subset construction
5. Use **⏭ Step** or **⚡ Auto** to animate
6. Go to **Minimize** tab → click **▶ Minimize**
7. Switch graph tabs to see NFA / DFA / Min-DFA
8. Go to **Simulate** tab → enter a string → click **Run**

---

## 🧠 Algorithms Implemented

| Algorithm | Complexity |
|-----------|-----------|
| ε-closure (per state) | O(n²) |
| Subset Construction (NFA→DFA) | O(2ⁿ · \|Σ\| · n²) |
| Hopcroft's Minimization | O(n · \|Σ\| · log n) |
| DFA String Simulation | O(\|w\|) |

Where `n` = number of NFA states, `Σ` = alphabet, `w` = input string.

---

## ✨ Features

- Step-by-step conversion with conversion log
- Auto-run with adjustable speed (100ms – 2000ms)
- Step counter and elapsed time tracker
- Live DFA transition table (builds as conversion runs)
- Export DFA as JSON
- Import NFA from JSON
- Input validation with inline error messages
- Dark / Light mode toggle
- Complexity statistics panel (actual vs worst case 2ⁿ)

---


