# The cooperative maximum capture facility location problem
### Concepción Domínguez, Ricardo Gázquez, Juan Miguel Morales, Salvador Pineda

This repository contains the instances used for the computational experiments of the titled paper: The cooperative maximum capture facility location problem.
A version of this paper can be found in ArXiv: 


The paper uses two data sets. A synthetic set, Syn-Data, generated randomly to compare the proposed approaches in order to determine the best one based on computational experience. Subsequently, we make a real application of the proposed model for the location of electric vehicle charging stations in the city of Trois-Rivières, Quèbec. For this purpose, we use the instance of the paper by Lamontagne et al (2022), and we upload here the parameters defined in our application.


- Syn-Data. The data folder contains the coordinates and weights of each user for each set. The locations folder contains the coordinates of the candidate locations. The epsilon folder contains the errors in the measurements, which follow a normal distribution for each scenario.
- Real-Data.  The data folder contains the coordinates and weights of each user. Since the candidate locations is a subset of the instance, the location folder contains the file with the indexes for the candidate positions. Epsilon contains the errors that follow a normal and a gumbell distributions. Kappa contains the distance term for each customer to the facility it considers, within a 10km radius.

Note that for Syn-Data there is no Kappas folder, since all distances from points to facilities are computed and distributed in quartiles, giving each distance a weight depending on the quartile (see the paper for more information). The function used to compute these distances was distance.minkowski for p = 2, from the scipy.spatial library.
