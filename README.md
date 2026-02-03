# Supply Chain Route Optimization – Vehicle Routing Problem (VRP)

This project solves a real-world delivery routing problem using a logistics distance dataset and two optimization approaches:
**Google OR-Tools** and **PuLP (MILP)**.  
The goal is to minimize total travel distance while respecting vehicle capacity and delivery time windows.

---

## Tech Stack
Python, Pandas, NumPy, Google OR-Tools, PuLP

---

## Problem
- One warehouse (depot)
- Multiple delivery locations
- Multiple vehicles
- Each location has a delivery demand and a service time window
- Each vehicle has limited capacity
- Objective: minimize total travel distance

---

## Steps Implemented

1. Load the logistics distance dataset (Excel).
2. Build a unified distance matrix including warehouse and all locations.
3. Add return-to-warehouse distances.
4. Create delivery demand for each location and define vehicle capacity.
5. Define delivery time windows for all locations.
6. Build and solve the VRP using **Google OR-Tools**  
   (distance, capacity and time-window constraints).
7. Formulate the same VRP as a **Mixed Integer Linear Program using PuLP**  
   (binary routing variables, capacity constraints and sub-tour elimination).
8. Extract and print the routes and total distance.

---

Result

Optimized total distance: 85 km

Naive baseline distance: 162 km

Distance reduced: 77 km (~47.5%)
