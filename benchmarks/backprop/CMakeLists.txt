cmake_minimum_required (VERSION 3.1)
project (libnvm-benchmarks)

set (THREADS_PREFER_PTHREAD_FLAG ON)
find_package (Threads REQUIRED)

find_package (CUDA REQUIRED)



make_benchmark (backprop-benchmark-module backprop-bench "main.cu;")

make_benchmark_choice (backprop-benchmark backprop-benchmark-smartio backprop-benchmark-module)
