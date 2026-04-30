# AP24110011033-ccc-end-sem-project
# 🚀 Smart Route Planner

## 📌 Project Description
The Smart Route Planner is a C-based project that demonstrates the use of two important algorithm design techniques:

- Greedy Algorithm → Dijkstra’s Algorithm  
- Dynamic Programming (DP) → Floyd Warshall Algorithm  

This project finds the shortest path between nodes in a graph.

---

## 🎯 Objectives
- Implement Greedy and Dynamic Programming algorithms
- Understand shortest path problems
- Build a menu-driven C program

---

## ⚙️ Algorithms Used

### 1. Dijkstra Algorithm (Greedy)
- Finds shortest path from a single source
- Chooses minimum distance node at each step
- Time Complexity: O(V²)

### 2. Floyd Warshall Algorithm (Dynamic Programming)
- Finds shortest paths between all pairs
- Uses intermediate nodes
- Time Complexity: O(V³)

---

## 🧩 Features
- Menu-driven program
- User input graph (adjacency matrix)
- Supports both algorithms
- Displays shortest paths clearly

---

## 🗂️ Folder Structure
Smart-Route-Planner/
│
├── src/
│   └── main.c
│
├── input/
├── output/
└── README.md

---

## ▶️ How to Run

1. Open terminal in src folder
cd src

2. Compile
gcc main.c -o main

3. Run
.\main.exe

---

## 🧪 Sample Input
4
0 5 0 10
0 0 3 0
0 0 0 1
0 0 0 0

---

## 🖥️ Sample Output
===== MENU =====
1. Dijkstra (Greedy)
2. Floyd Warshall (DP)
3. Exit

---

## 📊 Comparison

| Feature      | Dijkstra        | Floyd Warshall |
|-------------|----------------|----------------|
| Type        | Greedy         | Dynamic Programming |
| Output      | Single Source  | All Pairs |
| Complexity  | O(V²)          | O(V³) |

---

## 👥 Team Members
- Your Name
- Member 2
- Member 3

---

## 📚 Applications
- GPS Navigation
- Network Routing
- Traffic Systems

---

## ✅ Conclusion
This project demonstrates how Greedy and Dynamic Programming approaches solve shortest path problems efficiently.
