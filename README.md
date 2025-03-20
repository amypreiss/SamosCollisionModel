# SamosCollisionModel
Collision model for raptors and wind turbines on Samos, an island in the Aegean Sea. This is a project for my Geographic Information System Internship.
Due to the lack of bird denisty data on the island, I have opted for a Monte Carlo Simulation approach. The code runs 10,000 random bird flights within set parameters (constant trajectory and height) to calculate a collision probability for a bird colliding with a wind turbine, based on its average wingspan and flight altitude range and wind turine dimesions. 
Note: an intersection between a bird’s flight trajectory with a rotor-swept area is a ‘given collision’.
Using QGIS, I noted the corner coordinates of the minimumum bounding recantangle, and the wind turbines. THe coorner coordinates defined the edges that the bird would randomly enter the area of interest. To ensure the bird was flying forwards, the bird would enter at a random point on a randomly chosen edge, and leave the rectangle at a random point of randomly chosen but different edge. The flight height was randomly chosen between a defined range for the specific species of bird. The bird's wingspan was incorporated into its trajecetory to increase the area suseptible to collision. 
The code runs 10,000 random bird flights. I then noted the probability and repeated this 10 times so I could calculate a mean and standard deviation.

In my investiagtion, I chose to only focus on raptors. This is because:
a) They are most at risk because they are long-lived species with relatively low reproductive rate. 
b) Their flying height range is more hazardous 
c) Larger wingspans.
The species I looked at were owls (Barn Owl, Eurasian Scops Owl, Long-Eared Owl, Tawny Owl, Eurasian Eagle-Owl, and Little Owl); falcons (Common Kestrel, Eleonora’s Falcon, Lesser Kestrel, and Peregrine Falcon); and eagles/hawks/kites (Cinereous Vulture, Common Buzzard, Eurasian Imperial Eagle, Eurasian Sparrowhawk, European Honey Buzzard, Golden Eagle, Lesser Spotted Eagle, Long-legged Buzzard, Short-toed Snake Eagle, Steppe Eagle)

The proposal for Samos outiles the use of 4 different types of tubines: 15 V90s, 2 V100s, 8 V110s, 32 V120s (57 turbines total); 8.3 turbines per km2. The are all isolated to Eastern Samos.

Results:
- Flight height has the dominating influence on collision probability compared to wingspan
- Wingspan has a secondary effect, and peaks around 1.5m
- Larger wingspans tend to have lower probabilities likely due to being associated with soaring above the rotor-swept zone
- V120 turbines have the highest collision probability due to the larger rotor-swept area
- Owls have the highest collision probabilities, likely due to their lower flying altitudes 
- Eagles/Hawks/Kites tend to have lower average probabilities, likely due to their higher flying altitudes 

Further investiagtions:
- Looking at and comparing more species
- How much would collision probabilities change with reducing the number of turbines?
- How much would collision probabilities change by changing the wind turbine dimesnions (rotot radium and hub height)?
