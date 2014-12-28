cmake_minimum_required(VERSION 2.8)
project(JuliaVC)

# julia install directory
set(JULIA_DIR "C:/Users/khkim/Julia-0.4.0-dev")

# 
include_directories(
	${JULIA_DIR}/include/julia
	# FIXME: cannot find uv.h in julia binary distribution
	C:/Users/khkim/julia/deps/libuv/include)

# embedding.c example from julia repository
add_executable(example embedding.c)