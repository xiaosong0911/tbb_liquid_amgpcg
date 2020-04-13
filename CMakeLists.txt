project(tbb_liquid_amgpcg)
find_package(TBB CONFIG REQUIRED)

include_directories(
	pcgsolver
	sparse
	)

add_executable(Fluid3D
	faithful_surfacing3.cpp
	fluidsim.cpp
	GeometricLevelGen.cpp
	levelset_util.cpp
	main.cpp
	makelevelset3.cpp
	marching_tiles.cpp)
target_link_libraries(Fluid3D
	PRIVATE TBB::tbb)

add_subdirectory(viewpls3D)
