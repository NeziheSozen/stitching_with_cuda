#set(CUDA_NVCC_FLAGS ${CUDA_NVCC_FLAGS};-arch=compute_20;-code=sm_20;-std=c++11)
set(CUDA_NVCC_FLAGS ${CUDA_NVCC_FLAGS};-m=32)
Include(../ParallelUtils.cmake)
enable_cuda_support()
cuda_add_executable(tryMemoryAllocationError.out tryMemoryAllocationError.cu)
