cmake_minimum_required(VERSION 3.15)

project(DeployDoxygenDocs LANGUAGES CXX VERSION 1.2.3)

add_executable(${PROJECT_NAME} main.cpp)

install(TARGETS ${PROJECT_NAME} RUNTIME DESTINATION bin)
#file(GLOB headers "*.h")
#message("headers=${headers}")
#install(FILES ${headers} DESTINATION include)

set(CPACK_GENERATOR DEB)

set(CPACK_PACKAGE_VERSION_MAJOR "${PROJECT_VERSION_MAJOR}")
set(CPACK_PACKAGE_VERSION_MINOR "${PROJECT_VERSION_MINOR}")
set(CPACK_PACKAGE_VERSION_PATCH "${PROJECT_VERSION_PATCH}")

set(CPACK_PACKAGE_CONTACT agar10@yandex.ru)

include(CPack)