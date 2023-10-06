# Genetic Algorithm Implementation for Traveling Salesman Problem

## Introduction
The Traveling Salesman Problem (TSP) is a quintessential optimization challenge entailing the discovery of the most economical route encompassing each city once before returning to the point of origin (Applegate et al.). This narrative elucidates the design and deployment of a Genetic Algorithm (GA) for solving the TSP, explicating key algorithmic components and the rationale behind pivotal design choices.

## Program Design and Implementation

### Representation of Cities and Distances
- **City Representation:** 
   - Cities are symbolized as instances of the `City` class, each possessing `x` and `y` coordinates (Mitchell).
   - The `City` class houses a `distance` method for Euclidean distance calculation to another city.

```python
class City:
    # ...
    def distance(self, city):
        # ...
```

### Encoding the Solution Space
- **Route Representation:**
   - Routes, representing specific sequences of cities, are encoded as lists of `City` objects (Whitley).

### Creation of Initial Population
- The `initial_population` method in the `GeneticAlgorithmTSP` class engenders an initial population of random routes by shuffling the city list (Holland).

```python
def initial_population(self):
    # ...
```

### Fitness Score Computation
- The fitness score, a reciprocal of the total route distance, is computed to evaluate routes (Goldberg).

```python
class Fitness:
    # ...
    def route_fitness(self):
        # ...
```

### Parent Selection Strategy
- A hybrid strategy of elitism and fitness proportionate selection is adopted to balance exploration and exploitation (Baker).

### Crossover Strategy
- Single point crossover is employed to engender offspring by melding genes from two parent routes (Spears and DeJong).

```python
def crossover(self, parent1, parent2):
    # ...
```

### Mutation Strategy
- Mutation is orchestrated by swapping cities at two randomly designated positions in a route, facilitating genetic diversity (Fogel).

```python
def mutate(self, route):
    # ...
```

### Next Generation Population
- The next generation is populated through a fusion of elitism and offspring created via crossover and mutation, fostering genetic diversity and convergence towards an optimal solution (Eiben and Smith).

```python
def next_generation(self):
    # ...
```

### Stopping Condition
- The algorithm is executed for a specified number of generations, offering a simplistic yet effective stopping criterion (Srinivas and Patnaik).

```python
for i in range(self.generations):
    # ...
```

### Other Design Choices and Configuration
- Various parameters like population size, elite size, mutation rate, and number of generations are configurable to tune the algorithm's performance.
- The algorithm's progress and the optimal route are visualized using Matplotlib, providing invaluable insights into the algorithm's operation and performance.

## Conclusion
This design of the Genetic Algorithm for the TSP offers a robust framework for tackling the problem. It allows for effortless adjustments and expansions, rendering it a versatile solution for the TSP and potentially other optimization quandaries.In a recent work, Zhang and Chung proposed a clustering-based adaptive mechanism for adjusting crossover and mutation probabilities in Genetic Algorithms, offering a fresh perspective on optimizing these pivotal parameters for better performance.

## References
- Applegate, David, et al. "The Traveling Salesman Problem: A Computational Study." Princeton University Press, 2006.
- Baker, J. E. "Adaptive Selection Methods for Genetic Algorithms." Proceedings of an International Conference on Genetic Algorithms and Their Applications, 1985, pp. 101-111.
- Eiben, Agoston E., and J. E. Smith. "Introduction to Evolutionary Computing." Springer, 2003.
- Fogel, David B. "Evolutionary Computation: Toward a New Philosophy of Machine Intelligence." IEEE Press, 2006.
- Goldberg, David E. "Genetic Algorithms in Search, Optimization, and Machine Learning." Addison-Wesley, 1989.
- Holland, John H. "Adaptation in Natural and Artificial Systems." University of Michigan Press, 1975.
- Mitchell, Melanie. "Genetic Algorithms: An Overview." Complexity, vol. 1, no. 1, 1995, pp. 31-39.
- Spears, William M., and Kenneth A. DeJong. "On the Virtues of Parameterized Uniform Crossover." Proceedings of the Fourth International Conference on Genetic Algorithms, 1991, pp. 230-236.
- Srinivas, M., and Lalit M. Patnaik. "Adaptive Probabilities of Crossover and Mutation in Genetic Algorithms." IEEE Transactions on Systems, Man, and Cybernetics, vol. 24, no. 4, 1994, pp. 656-667.
- Whitley, Darrell. "A Genetic Algorithm Tutorial." Statistics and Computing, vol. 4, no. 2, 1994, pp. 65-85.
- Zhang, Jun, and Henry Shu-Hung Chung. "Clustering-Based Adaptive Crossover and Mutation Probabilities for Genetic Algorithms." IEEE Transactions on Evolutionary Computation, vol. 11, no. 3, 2007, pp. 326-335.


![Scatter_plot_](https://github.com/S-abk/GA_TSP/assets/117982032/dace638a-1f79-475c-9290-e434760d79f8)
![Scatter_plot](https://github.com/S-abk/GA_TSP/assets/117982032/9fb90bef-d0ae-40ab-b6df-bce57145ca88)
![Progress_plot](https://github.com/S-abk/GA_TSP/assets/117982032/efcf7623-674c-49f8-8b7f-cad5d2f4ca04)
![Progress_Plot](https://github.com/S-abk/GA_TSP/assets/117982032/2052e3ba-f9ca-49b5-9798-571661b31a04)



