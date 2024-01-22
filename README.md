# GPU vs CPU Performance Comparison

This project compares the performance of a Laplacian stencil computation on a CPU and a GPU using Numba and CUDA. The goal is to analyze execution time and memory usage on both devices.

## Laplacian Stencil

The Laplacian stencil is a common numerical computation used in image processing and simulations. It calculates the discrete Laplacian of a 2D array.

## Code Overview

The project includes:

- `laplacian_2d_stencil`: CPU implementation using Numba's stencil decorator.
- `laplacian_2d_cpu`: CPU implementation using Numba's njit decorator.
- `laplacian_2d_kernel`: GPU implementation using CUDA.

## Requirements

- Python 3.8 or >
- Numba
- CUDA-enabled GPU (for GPU execution)

## Numba

[Numba](http://numba.pydata.org/) is a high-performance, open-source JIT compiler that translates Python functions into optimized machine code. It is used in this project to accelerate the Laplacian stencil computation on both CPU and GPU.

## NumPy

[NumPy](https://numpy.org/) is the fundamental package for scientific computing with Python. It provides support for large, multi-dimensional arrays and matrices, along with mathematical functions to operate on these arrays.

## CUDA

[CUDA](https://developer.nvidia.com/cuda-zone) is a parallel computing platform and programming model developed by NVIDIA. It enables developers to use NVIDIA GPUs for general-purpose processing (GPGPU). In this project, CUDA is utilized for GPU acceleration.

## Results

The project provides insights into:

- Execution time comparison between CPU and GPU.
- Memory usage comparison between CPU and GPU.
- The speedup factor, indicating how many times faster the GPU is compared to the CPU.

## Performance Plot

The README includes a performance comparison plot, showcasing execution time and memory usage on both devices.
![image](https://github.com/Marinto-Richee/2D-Stenciling-using-CUDA-and-CPU/assets/65499285/09418ac1-3fcb-4f54-be8a-4df327b2b96d)
