# MARLM-SR
This is code page for paper "Learning Multiple Coordinated Agents under Directed Acyclic Graph Constraints" submitted to ICLR 2024.
For confidentiality reasons, we offer only three artificial environments in our repository.

The code is based on the [ray/rllib framework](https://docs.ray.io/en/latest/rllib/index.html) with the support of the Python/TensorFlow framework.

## Environments
You can find the details of the three implemented environments in the Appendix of the submitted paper.

### Factory production planning
Set the model and environmental settings in **Factory_production_planning.py**, and then run this Python file.

### Logistics
Set the model and environmental settings in **Logistics.py**, and then run this Python file.

### Hierarchical predator-prey
Set the model and environmental settings in **Hierarchical_predator_prey.py**, and then run this Python file.

## Code structure
### Factory production planning
In **multiagent/scenarios**: the basic components of each environment are defined.

**multiagent/core_{environment name}.py**: defines agents and environment.

**multiagent/env_{environment name}.py**: provides environments for the main algorithm MARLM-SR based on ray/rllib framework.

**multiagent/scenario_{environment name}.py**: provides basic functions for environments.

In **rllib_mod**: trainer is defined based on proximal policy optimization algorithm.

In **utils**: logger is defined to record learning curve based on reward.


