cmake_minimum_required(VERSION 3.3)

project(boost_type_traits)

add_library(boost_type_traits INTERFACE)

target_include_directories(boost_type_traits BEFORE INTERFACE ${CMAKE_CURRENT_SOURCE_DIR}/include)

install(TARGETS boost_type_traits DESTINATION lib)
install(DIRECTORY ${CMAKE_CURRENT_SOURCE_DIR}/include/boost DESTINATION include)

add_library(boost::type_traits ALIAS boost_type_traits)
