# Parsers

This repository contains two educational parser implementations commonly studied in automata theory and compiler design courses:

1. A **Regular Language Parser** based on **Deterministic Finite Automata (DFA)** using Python.
2. A **Shift-Reduce Parser** for simple grammars, implemented in C++.

Each parser includes test data and configuration files for demonstration purposes.

---

## 📁 Directory Structure

### 🔹 1. `Regular Language Parser/`

This directory implements a **DFA-based simulator** that reads a configuration file describing the automaton and evaluates whether a given input string is accepted.

#### 📄 Contents

| File Name                  | Description                                                                 |
|---------------------------|-----------------------------------------------------------------------------|
| `automata_demo.py`        | Basic DFA simulator using hardcoded transition functions.                   |
| `automata_demo_extended.py` | Extended DFA simulator that reads transitions, initial state, and final states from an external file (`model2.txt`). |
| `model.txt/model2.txt`      | Primary test files used with `automata_demo_extended.py`. Contains full DFA config (transitions, initial state, final states). |

### 🔹 2. `Shift_Reduce_Parser/`

This directory contains a Shift-Reduce Parser for a simple grammar, implemented in C++. It uses a parsing table and rule set to process and reduce input strings.

#### 📄 Contents
| File Name                 | Description                                                    |
| ------------------------- | -------------------------------------------------------------- |
| `Shift_Reduce_Parser.cpp` | Main C++ implementation of the shift-reduce parser.            |
| `Parsing Table.csv`       | Parsing table defining actions (shift, reduce, accept, error). |
| `Rules.txt`               | List of grammar rules used for reductions.                     |

## 🧠 Learning Goals
- Understand how DFA-based regular language parsers simulate recognition of regular languages.
- Explore the mechanics of bottom-up parsing via the Shift-Reduce technique.
- Gain exposure to parsing table construction, rule-based reduction, and stack-driven parsing logic.
