cmake_minimum_required(VERSION {{cookiecutter.cmake.minimum_version}})

project({{cookiecutter.project_name}} CXX)

set(CMAKE_CXX_STANDARD {{cookiecutter.cxx_standard}})

file(GLOB sources {{cookiecutter.sources_folder}}/*.cpp)
file(GLOB headers {{cookiecutter.include_folder}}/*.hpp)

add_executable({{cookiecutter.project_name}} ${sources} ${headers})

target_include_directories({{cookiecutter.project_name}} PUBLIC
    {{cookiecutter.include_folder}}/
)
