cmake_minimum_required(VERSION {{cookiecutter.cmake.minimum_version}})

project({{cookiecutter.project_name}} C)

file(GLOB sources {{cookiecutter.sources_folder}}/*.c)
file(GLOB headers {{cookiecutter.include_folder}}/*.h)

add_executable({{cookiecutter.project_name}} ${sources} ${headers})

target_include_directories({{cookiecutter.project_name}} PUBLIC
    {{cookiecutter.include_folder}}/
)
