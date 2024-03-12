# Budget Allocation with Citizen Preferences

This code tackles a resource allocation problem where a budget needs to be distributed among various issues while considering citizen preferences. It utilizes a network flow approach to find a feasible decomposition, ensuring all funds are allocated while respecting both individual interests and limitations on issue budgets.

## How it Works

The code defines a function called find_decomposition that takes two arguments:

budget: A list containing the available budget for each issue.

preferences: A list where each element is a set representing the issues a particular person is interested in.

## The function works by:

Calculating total budget and number of entities involved
Creating a directed flow network with nodes representing:
Source (starting point of the budget)
Destination (endpoint for allocated budget)
Each citizen
Each issue Edges connect these nodes with capacities based on budget constraints and preferences.
Finding the maximum flow through the network using NetworkX's edmonds_karp algorithm. This determines how much budget can be allocated while respecting capacity limits.
Analyzing the flow and checking for decomposition:
The code verifies if the total flow value matches the total budget, indicating successful allocation.
It also provides options to visualize the flow network (commented out by default).
