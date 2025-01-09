# Emergency Evacuation Optimization

This project was developed by Gonçalo Casanova Brito as part of the Optimization Methods for Management course. The aim is to solve a real-world optimization problem involving the evacuation of a region under the threat of a dam collapse.

## Problem Description

A region facing a potential dam rupture must be evacuated within a maximum of ten hours. The population includes:
- 8,000 men
- 7,900 women
- 1,850 children

Each person may carry up to 10 kg of personal belongings. The region is isolated, and only authorized vehicles are allowed to minimize accidents and traffic congestion.

### Constraints:
- Children must travel with their mothers.
- Vehicle types include private cars, buses, and helicopters.
- Vehicles can only make a limited number of trips.
- Private cars must stay outside the danger area after completing a trip.

The goal is to create a program that minimizes the total costs of the evacuation.

## Methodology

The optimization problem was modeled and solved using the Gurobi optimization library. Key components include:

### Decision Variables:
- **Xijk**: The type of family `i` transported in vehicle `j` during trip `k`.
- **Yjk**: A binary variable indicating if vehicle `j` is used for trip `k`.

### Objective Function:
Minimize the total cost of the evacuation.

### Constraints:
- Number of families transported.
- Vehicle capacity for passengers and luggage.
- Maximum number of trips per vehicle type.
- Ensuring safety and operational feasibility.

## Results

### Initial Scenario:
The optimal solution achieved a cost of €3,140.

### Updated Scenario:
After adjusting for increased fuel costs and vehicle maintenance, the optimal solution cost increased to €5,142, reflecting a rise of €2,002.

## Dependencies

- Python 3.8+
- Gurobi Optimizer 11.0.0
- pandas
- matplotlib

Install dependencies using:
```bash
pip install -r requirements.txt
