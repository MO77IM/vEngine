file(GLOB V_ENGINE_SOURCE ./src/*.cpp)
file(GLOB V_ENGINE_HEADER ./src/*.h)

source_group("Header Files" ${V_ENGINE_HEADER})
source_group("Header FIles" ${V_ENGINE_SOURCE})

#set(CMAKE_MODULE_PATH "${CMAKE_SOURCE_DIR}/3rdParty/freeglut/FreeGLUT")

set(FreeGLUT_DIR ${LIB_ROOT_DIR}/freeglut)
find_package(FreeGLUT CONFIG REQUIRED)

add_executable(vEngine ${V_ENGINE_SOURCE} ${V_ENGINE_HEADER})

target_link_libraries(vEngine PRIVATE freeglut)
