---
layout: page
permalink: /research/
title: research
description: Nonlinear dynamics, stochastic systems, physical computing, and modelling from data.
nav: true
nav_order: 1
---

My research starts with the dynamics of physical systems: how they switch, synchronize, fluctuate, and respond to interactions. A recurring question is how that behaviour can be used to perform a function. I work between numerical models and physical experiments, with **noise-aided computation** as the central thread.

## Can noise help a system compute?

A bistable system can occupy either of two states. Noise can make it switch between them; inputs and coupling can influence those switches. In our work, we arrange these ingredients so that the resulting behaviour implements logical operations.

This was the core of my PhD and early postdoctoral research, building on the noise-aided logic programme of my PhD supervisor, Sudeshna Sinha, and experimental collaborator K. Murali. I have driven modelling and investigations of coupled noisy systems, connecting numerical results with proof-of-principle electronic experiments.

Two examples show how the idea develops:

- **Logic through synchronization.** The collective state of two coupled bistable systems encodes a logical output. Adjusting bias and coupling allows different logic functions, with reliable operation in a suitable range of noise strengths. [Read the paper](https://doi.org/10.1103/PhysRevE.104.064207) · [PDF](/assets/pdf/emergent.pdf)
- **Invertible logic.** Fixing the inputs yields a logical output; fixing the output lets the system explore compatible inputs. Coupled noisy elements act as probabilistic bits, demonstrated numerically and in electronic circuits. [Read the paper](https://doi.org/10.1103/PhysRevApplied.20.034041) · [PDF](/assets/pdf/inverse_logic.pdf)

These experiments establish computational principles and the conditions under which they work. They are a foundation for asking how physical dynamics can be organized for computation.

## What changes when we change the interactions?

Coupling can produce collective behaviour that an isolated system cannot exhibit. I have studied how the timing of interactions, the distribution of frequencies, and correlations in noise alter that behaviour.

### Synchronization through frequency shuffling

Can exchanging frequencies among oscillators help them synchronize? Our study showed that repeated shuffling can lower the coupling needed for synchronization, connecting numerical work and theory with electronic oscillator experiments.

The initial idea came from **Vaibhav Pachaulee**, whose MSc research I mentored. I helped develop and lead the project, designed and supported the experimental implementation, guided the research, and contributed to its framing and writing. We brought in theoretical collaborators to develop the mathematical analysis.

[Read the paper](https://doi.org/10.1103/PhysRevE.109.L052302)

### Intermittent interactions and correlated noise

In coupled Chua circuits, we showed how making interactions intermittent in time or dependent on the system state can suppress or stimulate oscillations. In coupled bistable circuits, we examined how repulsive coupling competes with correlated noise to produce synchronization, anti-synchronization, and switching between them.

[Intermittent interactions](https://doi.org/10.1103/PhysRevE.106.014203) · [Coupling and correlated noise](https://doi.org/10.1063/5.0056173)

### How quickly can a system settle?

At Constructor University, I studied relaxation in heteroclinic networks with Hildegard Meyer-Ortmanns. These systems move through sequences of states. We investigated how they settle after a parameter change, and how network structure, coupling, and noise affect the relaxation time. This connects my interest in transient dynamics with questions about responsiveness and the persistence of dynamical states.

[On relaxation times of heteroclinic dynamics](https://doi.org/10.1063/5.0166803) · [PDF](/assets/pdf/heteroclinic_relaxation.pdf)

## What can observations tell us about the dynamics?

In our work on sleep onset at FEMTO-ST, we used a noisy bistable model to describe transitions in EEG activity. Parameters were inferred from experimental recordings using Markov chain Monte Carlo, connecting a dynamical description with observed variability.

I contributed to developing and interpreting the model, and helped mentor **Zhenxing Hu**, the first author, in collaboration with Jean-Julien Aucouturier, J. Nathan Kutz, and Xu Lei. My role drew particularly on stochastic dynamics and on making physical sense of the inferred parameters.

This project extended my work into modelling from observations. I am interested in developing that connection further; my experience here is in collaborative dynamical modelling and interpretation.

[Learning the bistable cortical dynamics of the sleep-onset period](https://doi.org/10.1371/journal.pcbi.1014246) · [Code and data](https://github.com/neuro-team-femto/cubic_sleep/)

## On the laboratory bench

Some of the systems I work with fit on a breadboard. Others have a flame.

Our ethanol-lamp study used a small lamp whose flame could be steady or flickering, depending on fuel volume and the number of wicks. Bringing lamps together produced in-phase and anti-phase oscillations, as well as suppression of oscillations. It is a tangible way to investigate collective dynamics with an accessible experimental system.

[Ethanol lamp: a simple, tunable flame oscillator and its coupled dynamics](https://doi.org/10.1140/epjs/s11734-021-00414-4) · [PDF](/assets/pdf/ethanol_lamp.pdf)

## Methods

My established tools include numerical modelling in Python and MATLAB, design and characterization of nonlinear electronic circuits, experimental automation, and data acquisition and analysis. Moving between simulation and experiment helps me examine which features of a model survive in a physical realization.

See the complete [publication list](/publications/) and [CV](/cv/).
