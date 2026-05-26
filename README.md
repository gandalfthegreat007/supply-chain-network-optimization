# Solar Supply Chain Network Optimization using MILP and Power BI

## Project Overview

This project develops a Mixed Integer Linear Programming (MILP)-based supply chain network optimization model for rooftop solar distribution across major Indian cities.

The model determines the optimal allocation of manufacturing facilities to demand locations while minimizing:

- Transportation Cost
- Variable Manufacturing Cost
- Fixed Facility Operating Cost

The project also evaluates multiple service-level scenarios to analyze the trade-off between customer service and total network cost.

---

## Business Problem

India’s rooftop solar market is expanding rapidly due to increasing renewable energy adoption and government initiatives. However, solar manufacturers and distributors face significant operational challenges in deciding:

- Where manufacturing/assembly facilities should operate
- How regional demand should be allocated
- How transportation costs can be minimized
- How service levels impact total network cost

This project simulates a realistic supply chain network design problem where candidate manufacturing locations are pre-identified, and the optimization model determines the most cost-efficient network configuration.

---

## Objective

The primary objective of this project is to minimize total supply chain cost while satisfying regional rooftop solar demand across India.

The optimization model considers:

- Transportation cost
- Production cost
- Fixed facility operating cost
- Capacity constraints
- Minimum utilization constraints
- Service-level requirements

---

## Optimization Logic

The problem is formulated as a Mixed Integer Linear Programming (MILP) model.

### Decision Variables

- Shipment quantity from manufacturing facility to demand city
- Binary facility activation variable

### Objective Function

Minimize:

- Transportation Cost
- Variable Production Cost
- Fixed Facility Cost

### Constraints

- Demand fulfillment constraints
- Facility capacity constraints
- Minimum utilization constraints
- Service-level constraints
- Oversupply prevention constraints

---

## Technologies Used

- Python
- PuLP
- Pandas
- NumPy
- Geopy
- Power BI
- MILP Optimization

---

## Key Features

- Facility location optimization
- Transportation cost engineering
- Geographic distance modeling
- Service-level scenario analysis
- Facility utilization analysis
- Sankey flow visualization
- Geographic demand allocation dashboard

---

## Scenario Analysis

The model evaluates multiple service-level scenarios ranging from:

- 40%-100%

This helps analyze the trade-off between:

- Customer service
- Facility utilization
- Total network cost
- feasible/infeasible

---

## Dashboard Preview

### Network Allocation Dashboard

![Dashboard](images/dashboard.png)

---

## Key Insights

- Higher service levels significantly increase total network cost, there is a significant increase in the cost after 0.7 service level due to addition of new unit (from 4-> 5)
- Ahmedabad emerged as the most strategically efficient manufacturing hub due to lower production and transportation costs
- Transportation cost contribution remained relatively low compared to production and fixed operating costs
- Some facilities experienced lower utilization under lower service-level scenarios
- The optimization model effectively balanced operational efficiency and customer service requirements
---

## Repository Structure

```text
solar-network-optimization-milp/
│
├── notebooks/
│   └── solar_network_optimization.ipynb
│
├── data/
│   ├── demand.csv
│   ├── plants.csv
│   └── circuity.csv
│
├── dashboard/
│   └── network_solar.pbix
│
├── images/
│   ├── dashboard.png
│   └── sl vs cost tradeoff.png
│
├── README.md
├── requirements.txt
└── .gitignore