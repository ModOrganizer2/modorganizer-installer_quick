cmake_minimum_required(VERSION 3.16)

find_package(mo2-cmake CONFIG REQUIRED)
find_package(mo2-uibase CONFIG REQUIRED)

add_library(installer_quick SHARED)
mo2_configure_plugin(installer_quick WARNINGS 4)
target_link_libraries(installer_quick PRIVATE mo2::uibase)
mo2_install_plugin(installer_quick)
