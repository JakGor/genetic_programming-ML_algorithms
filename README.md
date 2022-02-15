# genetic_programming-ML_algorithms
Final project for the course 'Genetic programming in Python'. I used idea of genetic program (a program which creates programs (code) for specific solution) to create algorithm, which automatically choose best Machine Learning technique for given dataset. Of course it isn't typical genetic programming - I'm not defining a primitive set as a tree or use specific libraries (such as DEAP) - I splitted a typical process of applying Machine Learning to a data to three parts:
* NA action - what to do with missing observations?
* outliers handling - what to do with exceeding observations?
* select algorithm - which Machine Learning algorithm should be used?

Whole process works as follows:
1. The fitness function is the Accuracy achieved finally by the given program
2. The initial population consists of 10 programs, the content of which is selected randomly
3. As a result of the selection, the best 6 individuals remain
4. 5 pairs of parents are selected by the tournament method
5. Children of a given pair of parents arise as a result of crossing the parents' genotypes
  a. The program has a specific crossover probability
  b. The crossing point can be anywhere in the genotype
  c. Crossbreeding gives two children
6. Every child can undergo a mutation
  a. Mutation occurs with a certain probability
  b. The presence of a mutation is manifested by the mutation flag changing from False to True
  c. A mutation results in a different classifier creation
7. 7 children with the best fit function values are selected
8. The new population is made up of selected children and the best parent
9. You go back to step 3 


