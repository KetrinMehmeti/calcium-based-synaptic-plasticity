# Calcium-Based Synaptic Plasticity in Spiking Neural Networks

**Neuroengineering group project | MSc in Information Bioengineering | Politecnico di Milano**

## Overview

This project explores **calcium-dependent synaptic plasticity** in spiking neural networks, with a focus on the mechanisms underlying **long-term potentiation (LTP)** and **long-term depression (LTD)**. We implemented custom neuron and synapse models using **NESTML**, simulated their dynamics with the **NEST Simulator**, and investigated how different synaptic mechanisms respond to pre- and postsynaptic spike timing.

The study compares a simplified plastic synapse, whose efficacy is controlled by a calcium-dependent state variable, with a more detailed synaptic model incorporating **vesicle availability and short-term synaptic dynamics**.

## Modeling Approach

- **Calcium-dependent neuron model:** AMPA/NMDA synaptic currents, voltage-dependent calcium influx, intracellular calcium dynamics, and a plasticity state governing synaptic efficacy.
- **Simplified synapse:** Synaptic weight varies with the postsynaptic plasticity state (`Syn_calcio.nestml`).
- **Vesicle-based synapse:** Extends the connection dynamics with resource availability and utilization variables, allowing recovery and facilitation effects (`Syn_tsodyks.nestml`).

We used timed pre- and postsynaptic stimulation protocols to explore potentiation and depression, recording membrane potential, calcium-related variables, and synaptic responses. The notebooks also contain example simulations with stochastic input.

## Repository Structure

| Path | Contents |
|---|---|
| [`Simulations/Neuro_calcio.ipynb`](Simulations/Neuro_calcio.ipynb) | Simulations using the simplified calcium-dependent synapse |
| [`Simulations/Neuro_va.ipynb`](Simulations/Neuro_va.ipynb) | Simulations using the vesicle-based synapse |
| [`Simulations/Neuro_calcio.nestml`](Simulations/Neuro_calcio.nestml), [`Neuro_va.nestml`](simulations/Neuro_va.nestml) | Custom neuron model definitions |
| [`Simulations/Syn_calcio.nestml`](Simulations/Syn_calcio.nestml), [`Syn_tsodyks.nestml`](simulations/Syn_tsodyks.nestml) | Custom synaptic model definitions |
| [`Media/project_presentation.mp4`](Media/project_presentation.mp4) | Group project presentation (approximately 3 minutes) |

## Tools & Technologies

- **Computational Neuroscience:** NEST Simulator, NESTML / PyNESTML
- **Programming & Numerical Computing:** Python, NumPy
- **Experiments & Visualization:** Jupyter Notebook, Matplotlib
- **Original Notebook Environment:** EBRAINS-24.04 kernel

## Simulation Results & Presentation

The notebooks contain simulated examples of potentiation- and depression-related dynamics under different spike-timing conditions.

**[Watch the project presentation](Media/project_presentation.mp4)** for an overview of the biological motivation, model design, and comparison of simulation outcomes.

## Running the Notebooks

The notebooks were developed in an **EBRAINS-24.04** environment. To run the simulations, a compatible installation of **NEST Simulator**, **PyNESTML**, and the required code-generation/build toolchain is needed, along with Python, NumPy, and Matplotlib.

Open the notebooks with `Simulations/` as the working directory, since they refer to the local `.nestml` files by filename. The notebooks first generate and install a NEST extension module before running the simulation experiments. The original notebooks preserve their plotted outputs, so the examples can also be inspected without running the model-generation steps.

## Contributors

Ketrin Mehmeti, Leonardo Giorgio Franco, Edoardo Franco Mattei, Gaia Crescini Parise, Andrea Ermacora.

Developed as part of the Neuroengineering coursework at **Politecnico di Milano**.
