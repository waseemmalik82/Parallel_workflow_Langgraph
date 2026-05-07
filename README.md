# ⚡ Parallel Workflows using LangGraph

This repository demonstrates how to build **parallel workflows** using LangGraph and Python. The project focuses on executing multiple workflow nodes simultaneously to improve efficiency, modularity, and structured AI pipeline design.

---

## 📂 Repository Structure

* `Batsman_Workflow.ipynb`
  → A cricket analytics workflow that processes batting statistics such as runs, fours, sixes, strike rate, and boundary percentage using parallel nodes.

* `PMS_essay_workflow.ipynb`
  → A workflow that generates structured PMS-style essays by processing multiple sections in parallel and combining them into a final response.

---

## 🚀 What You’ll Learn

* Building **parallel execution workflows** in LangGraph
* Managing shared workflow state
* Running independent nodes simultaneously
* Combining outputs from multiple nodes
* Error handling and state debugging in LangGraph
* Designing modular AI pipelines

---

## 🛠️ Technologies Used

* Python 🐍
* LangGraph
* LangChain
* Jupyter Notebook

---

## 🧠 Key Concepts

### 🔹 Parallel Workflow Execution

Instead of running nodes one-by-one, multiple tasks execute simultaneously and their outputs are merged into a shared state.

### 🔹 State Management

LangGraph uses shared state objects to pass and combine data between nodes.

### 🔹 Workflow Orchestration

Different processing steps are coordinated together to create scalable AI workflows.

---

## 📊 Example Workflow

### Cricket Analytics Workflow

The workflow:

1. Takes batting statistics as input
2. Calculates strike rate
3. Calculates boundary percentage
4. Merges all outputs into a final state

Example input:

```python id="1q88pj"
initial_state = {
    'runs': 75,
    'balls': 50,
    'fours': 6,
    'sixes': 4
}
```

---

## ⚠️ Common Error

If you encounter:

```text id="v7uvxg"
TypeError: 'int' object is not callable
```

It usually means a multiplication operator `*` is missing.

### ❌ Wrong

```python id="d1ml5l"
(boundaries / total_runs)(100)
```

### ✅ Correct

```python id="tmjlwm"
(boundaries / total_runs) * 100
```

---

## 💡 Future Improvements

* Add conditional routing workflows
* Integrate external APIs
* Build multi-agent systems
* Add Streamlit or FastAPI interface
* Deploy workflows as AI services

---

## 👨‍💻 Author

**Waseem Malik**
GitHub: https://github.com/waseemmalik82

---

## ⭐ Support

If you found this project helpful, consider giving the repository a star ⭐
