# Smart Wi-Fi Router Placement Using Jaya Algorithm

## Project Overview
This project demonstrates how to **optimize the placement of a Wi-Fi router** in a small office or café to maximize the signal coverage for all users.  
The optimization is performed using the **Jaya Algorithm**, a parameter-less evolutionary computation technique that iteratively moves candidate solutions towards the best and away from the worst solution.  

The goal is to find the optimal `(x, y)` position for the router that **maximizes the average signal strength** received by all users.

---

## Problem Statement
In a real-world environment:
- Users are distributed across a 2D space (office, café, or room).  
- Signal strength decreases with distance from the router.  
- Placing the router at a suboptimal location results in **poor connectivity** for some users.

The **objective function** models the Wi-Fi signal as inversely proportional to the square of the distance:

\[
f(x, y) = \sum_{i=1}^{N} \frac{1}{(x - x_i)^2 + (y - y_i)^2 + \epsilon}
\]

Where:
- `(x_i, y_i)` are the user positions
- `ε` is a small constant to avoid division by zero  
- The algorithm **maximizes** this function (or minimizes `-f(x, y)` in implementation).

---

## Jaya Algorithm Overview
**Jaya** is an evolutionary optimization algorithm that works as follows:
1. Initialize a population of candidate solutions (router positions).  
2. Evaluate the fitness (signal strength) of each candidate.  
3. Identify the **best** and **worst** candidates.  
4. Update all candidates by moving towards the best and away from the worst.  
5. Repeat until convergence or a maximum number of iterations.  

**Advantages:**
- No algorithm-specific parameters (like mutation or crossover rates)  
- Simple to implement  
- Efficient for continuous optimization problems like router placement

---

## How to Use
1. Open the notebook in Google Colab:  
[Open in Google Colab](https://colab.research.google.com/github/<your_username>/Smart-WiFi-Router-Placement/blob/main/Smart_WiFi_Router_Placement.jynb)  

2. Execute the notebook step by step:
   - Define the **positions of users**  
   - Run the **Jaya Algorithm**  
   - Visualize the **convergence curve**  
   - Visualize the **optimal router placement** in 2D  

3. Modify parameters as needed:
   - Number of users  
   - Population size  
   - Iterations  
   - Bounds of the 2D space

---

## Results
- **Convergence Curve:** Shows how the average signal strength improves over iterations.  
- **2D Visualization:** Users are shown as blue dots, and the optimal router position is shown as a red star.  

### Example Output
