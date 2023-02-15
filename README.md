# Resources for Mini-iGEM 2023 – Team 5: E.consortia
## [References](References.md)
References used for the project can be found in the [References.md](References.md) file

## Code
The Python code used for the modelling of our co-culture system can be found in the "placeholder.py"

The file contains the code for the following models:
1. Gene expression in individual cells
2. Agent-based population model
3. Classifier model (specificity & sensitivity of detection by killer strain)

Models of the inner circuit of each cell and of the entire reactor were made to verify good functioning of chosen parts and to modulate the system accordingly. Models were coded in Python.

Each cell contained an ODE system that described the production rate of the mRNA of each cassette and each of the relevant protein amounts. Parameters were chosen so that a single time step corresponded to a minute. This was solved using the scipy.odeint function. 
The core of the ODE system was an adapted bistable switch that responds to a decline in the copy number of cassette 1 by further repressing cassette 1 expression and expressing the BamAe.

The reactor was conceived of as a turbidostat with a constant number of cells. After each time step replication events were considered and then a random sample of cells were diluted out to return the population to the desired population amount. Depending on the internal ODE systems, Producer cells expressed a certain amount of the BamA epitope, Killer cells had a likelihood of binding to cells based on their BamA epitope expression. The chance that this binding leads to death is a function of the Producer’s cdiI concentration.

## Protein Folding
The folder "BamAe Protein Folding & Docking" contains the results and methodology of modelling BamA-epitope transmembrane protein folding and docking.
