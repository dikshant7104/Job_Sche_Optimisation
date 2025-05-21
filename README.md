# Job Scheduling Optimisation Project

## Overview

This project explores job scheduling optimisation in a small workshop environment where jobs must pass through four machines in a defined sequence. The primary goal is to minimise the overall completion time (makespan) using two algorithmic approaches:

* Greedy Algorithm
* Ant Colony Optimisation (ACO)

Developed as part of MSc. Data Analytics coursework at the National College of Ireland.

## Problem Description

* **Scenario**: 5 jobs processed on 4 machines in fixed order.
* **Objective**: Minimise makespan (maximum job completion time).
* **Randomness Control**: Seed value `3146` used for reproducible results.

### Input Processing Time Matrix:

```
[[2, 7, 6, 9],
 [3, 2, 5, 6],
 [1, 4, 1, 8],
 [2, 4, 2, 2],
 [9, 5, 2, 7]]
```

## Algorithms Implemented

### Greedy Algorithm

* Selects the earliest available machine for each job.
* Makes quick decisions without considering future impact.
* Fast and simple to implement.
* **Result**:

  * Makespan: `3`
  * Runtime: `0.005 seconds`

### Ant Colony Optimisation (ACO)

* Bio-inspired metaheuristic algorithm mimicking ant foraging.
* Balances exploration and exploitation via pheromone updates.
* Customisable parameters (number of ants, alpha, beta, evaporation rate).
* **Result**:

  * Makespan: `3`
  * Runtime: `0.0139 seconds`

## Tools & Libraries

* **Python**
* **PuLP**: Linear programming modeling library.
* **time**, **random**: For performance measurement and stochastic behavior.

## Results Comparison

| Algorithm       | Makespan | Runtime (s) | Comments                          |
| --------------- | -------- | ----------- | --------------------------------- |
| Greedy          | 3        | 0.005       | Fast, less adaptive to complexity |
| Ant Colony Opt. | 3        | 0.0139      | Better exploration, more robust   |

## Observations & Improvements

* Improve greedy algorithm by incorporating priority queues.
* Refine output formatting for readability.
* Address initial job wait times (`inf`) in ACO output.
* Experiment with ACO parameters to optimise results.
* Perform sensitivity analysis to evaluate algorithm robustness.

## Conclusion

* **ACO** excels in complex scheduling by finding high-quality solutions.
* **Greedy** is ideal for faster results in simpler scheduling problems.
* Choice between algorithms depends on trade-offs between speed and solution quality.

---

Developed by: **Dikshant Manohar Bhosale**
