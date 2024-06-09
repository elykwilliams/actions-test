cmake_minimum_required(VERSION 3.15...3.28)

project(MPI_Test C)

find_package(MPI COMPONENTS C REQUIRED)

add_executable(test_mpi main.c)
target_link_libraries(test_mpi MPI::MPI_C)

