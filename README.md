# GeoBench

**GeoBench: New HPC Architectures for Geosciences** is a benchmark suite designed to evaluate the performance and scalability of modern computing platforms in geoscientific workloads. It includes representative kernels from seismic imaging, reservoir simulation, and AI-based geoscience models.

## Objective

GeoBench aims to assess how effectively emerging computing platforms can address the computational demands of key geoscientific tasks. By focusing on critical operations and real-world kernels, this benchmark suite helps guide architecture evaluation and system design in domains such as seismic imaging, reservoir modeling, and machine learning for geosciences.

The benchmark suite will also define a set of metrics to compare different hardware and software platforms in terms of performance, efficiency, and scalability.

## Benchmark Categories

The suite is organized into three categories:

### 🧭 Seismic Exploration

1. **Wave Propagation — `miniwave`**  
   A stencil-based PDE kernel used in forward modeling for seismic imaging techniques like RTM and FWI.  
   [Repo: `simwave`](https://github.com/LSC-Unicamp/simwave)

2. **Reverse Time Migration (RTM)**  
   *To Be Defined* — A simplified RTM workflow involving backward propagation and imaging condition.

3. **Full Waveform Inversion (FWI)**  
   *To Be Defined* — A benchmark focusing on gradient computation via the adjoint-state method.

### 🛢️ Reservoir Simulation

1. **Sparse Matrix-Matrix Multiplication (SpMM) Kernel**  
   Extracted from the [OPM Flow](https://opm-project.org/?page_id=19) reservoir simulator.  
   [Repo: `opm-simulators`](https://github.com/OPM/opm-simulators)

2. **Linear Solver**  
   Also extracted from OPM Flow, this benchmark targets iterative solvers (e.g., CG, BiCGStab) used in large-scale reservoir simulation workflows.

### 🤖 AI for Geosciences

1. **UNet 3D**  
   A volumetric convolutional network used in seismic data interpretation, such as facies classification or image translation.

2. **Fourier Neural Operator (FNO)**  
   A model for learning mappings between function spaces, suitable for data-driven PDE solutions and surrogate modeling.  
   [Library: `neuraloperator`](https://github.com/neuraloperator/neuraloperator)

## Key Features

- Domain-relevant kernels designed for seismic and reservoir workflows
- Benchmarks include both classical simulation kernels and AI-driven models
- Open, modular, and extensible design
- Performance metrics and evaluation methodologies to be defined as part of the project

---

Each benchmark will be accompanied by setup instructions, datasets (if applicable), and performance profiling scripts.

Contributions and feedback are welcome as we continue to expand and refine GeoBench.
