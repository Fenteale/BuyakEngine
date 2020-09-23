set(CMAKE_CXX_STANDARD 17)

set(SOURCES
		main.cpp
		main.h)

find_package(OpenGL REQUIRED)
find_package(GLUT REQUIRED)

include_directories( ${OPENGL_INCLUDE_DIRS} ${GLUT_INCLUDE_DIRS})

add_executable(${PROJECT_NAME} ${SOURCES})

target_link_libraries(${PROJECT_NAME} PUBLIC ${OPENGL_LIBRARIES} ${GLUT_LIBRARY} assimp)