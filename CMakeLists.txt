cmake_minimum_required(VERSION 3.15...3.28)

project(MPI_Test C)

find_package(MPI COMPONENTS C REQUIRED)

add_executable(test_mpi main.c)
target_link_libraries(test_mpi MPI::MPI_C)

enable_testing()
add_test(NAME run_mpi_test COMMAND "mpirun -np 2 $<TARGET_FILE:test_mpi>")