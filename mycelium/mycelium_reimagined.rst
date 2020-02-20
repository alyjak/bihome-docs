###########################
Mycelieum/BiHome Reimagined
###########################


This twitter thread made me realize that a unifying theme of my interests is the creation of
positive feedback loops. Positive feedback looks are what I look to create at work, and they drive
much of my interest in permaculture. In this thread, the author made me remember that feedback loops
can be appropriately modelled without encoding all the system details. Instead knowledge of circuit
diagrams is key:

https://twitter.com/BuildSoil/status/1086728146294980608?s=20


This helps clarify what I hope to accomplish with bihome. Fundamentally I want to help create
positive feedback loops in a suburban setting. The units I hope to to create positive feedback on
are:

- Biodiversity
- Yield fit for human consumption
- Soil health

The units I want to minimize upkeep costs are:

- human labor/year
- dollars/year

My prior approach to this was to start from simulating as close as I can to first principles --
essentially creating a valid enviromental simulation -- and then run a type of monte carlo
evolutionary algorithm in the simulation in order to discover novel scenarios for stewarding the
land. I was going to start by making an L-systems simulator in rust, a la 

Now, I think a better approach would be: start as close to circuit diagrams as possible, then run
the evolutionary monte carlo to discover novel scenarios and combinations.

The app would consist of:

1. A wiki website that maps species to their fundamental open system model.
2. A construction UI for modelling a local ecosystem based on the units available via the wiki
   (initial model size on the order of a garden bed to start, possibly then creating a fractal
   network of larger models based on using those smaller models as base units).
3. A simulation engine that, when run, performs stepwise modifications to a closed model. Models are
   closed by hooking up a constructed model to the "world model". The world model supplies weather,
   base inputs, and tracks outputs.
4. A set of optimization algorithms, starting with the evolutionary monte carlo approach that
   performs step wise tweaks to a closed model -- either introducing new items, removing items, or
   tweaking an items parameters in order to determine systematic effects.


First step here would be to create some systems modelling capabilities -- I think I still like my
choice of Rust + ECS as the sim engine for this.

***************
possible issues
***************

- modelling piece-wise with these circuit constructs is difficult because:

  - inputs and outputs often are connected through diffusion relationships
  - How do you validate or even construct a single plant system diagram?
  - organisms are stateful - the function and magnitude of their system relationships changes over
    time
