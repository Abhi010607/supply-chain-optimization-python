#  Supply Chain Network Optimization using Python

##  Overview
This project focuses on optimizing a supply chain distribution network for a smart wearable device company (“Blink”). The goal is to determine the most cost-efficient transportation plan from multiple assembly plants to different demand regions.

The optimization model minimizes total transportation cost while ensuring that all regional demands are satisfied.

---

##  Objective
Minimize total transportation cost based on:
- Distance between assembly plants and regions
- Cost per unit per mile
- Demand requirements at each region

---

##  Problem Description

Blink operates:
- 2 Assembly Plants  
- 3 Demand Regions  

### Monthly Demand (Units)
- Region 1: 2500  
- Region 2: 4350  
- Region 3: 3296  

### Distance Matrix (Miles)

| From / To | Region 1 | Region 2 | Region 3 |
|----------|----------|----------|----------|
| Plant 1  | 105      | 256      | 86       |
| Plant 2  | 240      | 136      | 198      |

### Transportation Cost
- $0.12 per unit per mile  

---

##  Mathematical Model

### Decision Variables
xᵢⱼ = Number of units transported from plant i to region j

### Objective Function
Minimize total transportation cost:

Z = Σ (xᵢⱼ × distanceᵢⱼ × 0.12)

### Constraints
- Demand satisfaction for each region  
- Non-negativity of decision variables  

---

##  Approach
- Formulated as a Linear Programming problem  
- Implemented using Python  
- Solved using optimization libraries (PuLP / OR-Tools)  
- Executed in Google Colab  

---

##  Results

The optimization model determined the most cost-efficient transportation plan across the supply chain network.

-  Minimum Transportation Cost: $136,507 per month  

### Optimal Allocation (Summary)
- Each region’s demand is fulfilled with minimum-cost routing  
- Shipments are primarily assigned from the nearest assembly plant to reduce cost  

This result demonstrates how linear programming can significantly improve logistics efficiency by eliminating unnecessary transportation expenses.

---

##  Key Insights
- Transportation cost is highly dependent on distance  
- Optimal solutions prioritize closer plant-region allocations  
- Linear programming helps eliminate inefficient routing  

---

##  Extensions
This model can be extended by:
- Adding plant capacity constraints  
- Introducing distribution centers  
- Considering multiple transportation modes  
- Performing sensitivity analysis on demand  

---

##  Tools & Technologies
- Python  
- Google Colab  
- PuLP / OR-Tools  
- NumPy / Pandas  

---

##  Repository Structure
- `transportation_optimization.ipynb` → Main notebook  
- `README.md` → Project documentation  

---

##  Attribution
This project is inspired by concepts from the MITx Supply Chain Analytics (SC0x) course and has been independently implemented and extended.
