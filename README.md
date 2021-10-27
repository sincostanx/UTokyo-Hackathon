# Hybrid Forecasting of Chaotic Processes
This repository contains implementations and presentation materials on our group research conducted as a part of the UTokyo IST Research Hackathon organized from September 20th – 24th, 2021.

A huge thanks to everyone involved in this project:
- Akshat Verma
- Pongsakorn Chairatanakul
- Alexander Thomas Magro (Mentor)
- Wentao Sun (Mentor)

## Overview
- We replicate the experiment to forecast a [Lorenz system](https://en.wikipedia.org/wiki/Lorenz_system) by using a hybrid model presented in [this paper](https://arxiv.org/abs/1803.04779). Specifically, we compare the performance of a traditional ESN model and a hybrid model (i.e. a combination between ESN and an imperfect knowledge-based model) on the generated benchmark data:

    - **Knowledge-based model**: an imperfect model of Lorenz system. Imperfections can be represented by a slight error in parameter **b** (as described in the paper) or a difference in timestep between the benchmark data and that of a knowledge-based model when we observe the system (our original work).
    - **Echo State Network (ESN)**: a simple model in reservoir computing. A simple explanation of the model is described [here](https://mantas.info/code/simple_esn/).
    - **Hybrid-Model**: a combination of knowledge-based model and ESN, proposed in the paper.

- We further investigate the performance of these models under a different type of imperfection, a difference in timestep. The experiment suggested that the hybrid model also outperform the original one.
- We study the relationship between the allocation ratio (time used knowledge-based model divided by ESN model) and valid time (time until predictions become diverged).
