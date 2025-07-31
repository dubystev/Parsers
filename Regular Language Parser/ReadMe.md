# DFA Simulator

This subproject simulates a **Deterministic Finite Automaton (DFA)**. The [Extended Version of the Automata Demo script](./automata_demo_extended.py)
python script reads its configuration from an external text file (e.g., "model2.txt") and evaluates whether a given input string is accepted by the automaton.

## 📄 File Structure: 'model2.txt'

The DFA configuration file is divided into **three sections**, separated by lines containing six asterisks ('******').

### 🔹 Section 1 – Transition Function

Each line defines a state transition in the format:


- 'current_state' and 'next_state' are integers.
- 'input_symbol' is a single character (e.g., '0', '1').
- This section ends at the first line of '******'.

### 🔹 Section 2 – Initial State

A single line containing the starting state of the DFA.

- Begins after the first '******'.
- Ends at the second '******'.

### 🔹 Section 3 – Final (Accepting) States

A space-separated list of one or more integers representing the final states of the DFA.

- Follows the second '******'.

---

## 🧪 Example Configuration: 'model2.txt'

```
1 0 1
1 1 2
2 0 3
2 1 4
3 0 7
3 1 8
4 0 5
4 1 6
5 0 7
5 1 8
6 0 5
6 1 6
7 0 1
7 1 2
8 0 3
8 1 4
******
1
******
5 6 7 8
```

- **Initial State:** '1'
- **Final States:** '5', '6', '7', '8'
- **Transitions:** For example, '(1, 0) → 1', '(1, 1) → 2', etc.

---

## ▶️ How to Use

1. Ensure the file 'model2.txt' is in the same directory as 'automata_demo_extended.py'.
2. Run the script:
   ```bash
   python automata_demo_extended.py
3. Enter a string of input symbols (e.g., 0110) when prompted.
4. The program will simulate the DFA and report whether the string is accepted or rejected.
