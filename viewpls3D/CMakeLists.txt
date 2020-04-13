find_package(GLUT REQUIRED)
find_package(GLEW REQUIRED)

add_executable(viewpls3D
	gluvi.cpp
	main.cpp
	render_particles.cpp
	shaders.cpp)
target_link_libraries(viewpls3D
	PRIVATE GLUT::GLUT GLEW::GLEW)
