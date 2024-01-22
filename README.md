# 2D Stenciling using CUDA and CPU

This project is a benchmark comparison of 2D stenciling operations performed on a CPU and a GPU using CUDA. The main operation is the calculation of the Laplacian of a 2D array, which is a common operation in image and signal processing.

## Project Structure

The project consists of a single Python script that performs the following tasks:

1. **User Input**: The script first asks the user if they want to print the details of the execution.

2. **Laplacian Calculation**: Two functions, `laplacian_2d_cpu` and `laplacian_2d_kernel`, are defined to calculate the Laplacian of a 2D array on the CPU and GPU respectively.

3. **Memory Usage Measurement**: The `measure_memory_usage` function is used to measure the memory usage of an object.

4. **Benchmark Execution**: The `run_benchmark` function runs the benchmark on the specified device (CPU or GPU) with a given array size. It measures the execution time, memory usage, and throughput (operations per second) of the Laplacian calculation.

5. **Benchmark Iteration**: The script iterates over different array sizes and devices, storing the results of each run in a list.

6. **Results Presentation**: Finally, the script calculates the speedup factor of the GPU over the CPU and presents the results in a pandas DataFrame.

## Results

### CPU Results:
![Results](Analysis Results\cpu.png)

### GPU Results:
![Results](Analysis Results\gpu.png)

### Speed-Up Factor:
The speed-up factor is calculated by dividing the execution time of the CPU by the execution time of the GPU for a given array size and ID.

| ID | CPU | GPU |
| 1 | i5-10300H CPU @ 2.50GHz with GTX 1650 | NVIDIA GeForce GTX 1650 |
| 2 | i5-10300H CPU @ 2.50GHz with GTX 1650 Ti | NVIDIA GeForce GTX 1650 Ti |
| 3 | Intel(R) Core(TM) i7-1065G7 CPU @ 1.30GHz | NVIDIA GeForce MX230 |
| 4 | i7-10750H CPU @ 2.60GHz with GeForce RTX 2060 | NVIDIA GeForce RTX 2060 |
| 5 | i7-10750H CPU @ 2.60GHz with GeForce RTX 2070 with Max-Q Design | NVIDIA GeForce RTX 2070 with Max-Q Design |
| 6 | 12th Gen Intel(R) Core(TM) i7-12700H | NVIDIA GeForce RTX 3050 Ti Laptop GPU |
| 7 | Intel(R) Xeon(R) CPU @ 2.30GHz | Tesla T4 |
| 1 | i5-10300H CPU @ 2.50GHz with GTX 1650 | NVIDIA GeForce GTX 1650 |
| 2 | i5-10300H CPU @ 2.50GHz with GTX 1650 Ti | NVIDIA GeForce GTX 1650 Ti |
| 3 | Intel(R) Core(TM) i7-1065G7 CPU @ 1.30GHz | NVIDIA GeForce MX230 |
| 4 | i7-10750H CPU @ 2.60GHz with GeForce RTX 2060 | NVIDIA GeForce RTX 2060 |
| 5 | i7-10750H CPU @ 2.60GHz with GeForce RTX 2070 with Max-Q Design | NVIDIA GeForce RTX 2070 with Max-Q Design |
| 6 | 12th Gen Intel(R) Core(TM) i7-12700H | NVIDIA GeForce RTX 3050 Ti Laptop GPU |
| 7 | Intel(R) Xeon(R) CPU @ 2.30GHz | Tesla T4 |

![Results](Analysis Results\Speed-up Factor vs Array Size.png)

## Usage

To run the benchmark, simply execute the script. You will be asked if you want to print the details of the execution. Enter 'y' for yes or 'n' for no.

## Requirements

This project requires Python, Numba, NumPy, and pandas. If you want to run the GPU benchmarks, you will also need a CUDA-capable GPU and the CUDA toolkit.
