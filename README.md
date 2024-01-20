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

- Python 3.x
- Numba
- CUDA-enabled GPU (for GPU execution)

## Results

The project provides insights into:

- Execution time comparison between CPU and GPU.
- Memory usage comparison between CPU and GPU.
- The speedup factor, indicating how many times faster the GPU is compared to the CPU.

## Performance Plot

The README includes a performance comparison plot, showcasing execution time and memory usage on both devices.
![image](https://github.com/Marinto-Richee/2D-Stenciling-using-CUDA-and-CPU/assets/65499285/09418ac1-3fcb-4f54-be8a-4df327b2b96d)
