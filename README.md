# HCU Land Dispute 

This repository contains a Jupyter Notebook that simulates and analyzes the **HCU land dispute controversy**, where protesters were arrested and later released under certain conditions. The project models the problem mathematically, demonstrates step-by-step reasoning, and visualizes the results using Python. (Note: This Problem was only taken for knowledge Purposes to learn and obtain the output through ML Process)

**Problem:**

During the HCU land dispute controversy, protests occurred from students and environmental activists. Therefore, the government decided to arrest the protesters (students and activists). Due to government orders, the police began arresting the protesters. However, the HCU police station has a capacity of only 100 cells, so they arrested 100 protesters. Each cell/prisoner was assigned numbers from 1 to 100. 

As days passed, the protesters approached the court. As a result, the court ordered the government to release the protesters. To resolve the issue, the government instructed the police to release the protesters with conditions. The government decided to send 100 representatives (MLAs) to the police station with specific instructions. 

Each MLA was assigned a number from 1 to 100. Each MLA inspected all the cells in the police station. If the cell number is divisible by the MLA number leaving no remainder, the MLA takes action.

The MLA's action is: if the cell is already closed, the MLA opens the cell, or if the cell is already open, the MLA closes the cell. After all the MLAs have walked through all the cells, the protesters requested to walk out of the police station only from the open cells. 

**Questions**: 

1) How many protesters are finally released?
2) List their respective cell/prisoner number(s).

---

## 📂 Repository Contents

- `HCU_Land_Dispute.ipynb` → Main notebook containing the explanation, logic, and plots.  
- `requirements.txt` (optional, can be added) → Python dependencies for easy setup.  

---

## 🚀 Features

- Simulation of prisoner cell toggling (arrests and releases).  
- Step-by-step explanation of the logic behind the process.  
- Graphs and plots to visualize how cells/prisoners change over time.  
- Easy-to-follow notebook structure with comments and outputs. 

--- 

**Step 1: Understanding in Simple Words**

- Imagine **100 prison cells** (numbered 1 to 100).
- At the start, **all are closed **(protesters are locked inside).
- Then **100 MLAs** (also numbered 1 to 100) take turns:
- MLA 1 toggles (opens/closes) **every cell** (because every number is divisible by 1).
- MLA 2 toggles every **2nd cell** (2, 4, 6, …).
- MLA 3 toggles every **3rd cell** (3, 6, 9, …).
- and so on, until MLA 100 toggles only cell 100.

**Key Rule:**

- If a cell is **closed**, the MLA opens it.
- If a cell is **open**, the MLA closes it.

---

**Step 2: What Happens?**

- A cell will be toggled once for every divisor it has.
- Example: Cell 12 → divisors are (1, 2, 3, 4, 6, 12). That’s 6 actions.
- If a cell has an odd number of divisors, it ends up open.
- If a cell has an even number of divisors, it ends up closed.
- 👉 **Only perfect squares **(1, 4, 9, 16, …, 100) have an odd number of divisors.

---

**Answers:**
1) 10
2) [1, 4, 9, 16, 25, 36, 49, 64, 81, 100]
