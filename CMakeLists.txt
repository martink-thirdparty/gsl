cmake_minimum_required(VERSION 3.5)

# transitive dependency check

if(TARGET gsl)
  return()
endif()

# project

project(
  gsl
  VERSION 3.1.0
  DESCRIPTION "Guidelines Support Library"
  HOMEPAGE_URL "https://github.com/microsoft/GSL"
  LANGUAGES CXX)

add_library(gsl INTERFACE)

# SDK

target_include_directories(
  ${PROJECT_NAME}
  INTERFACE $<BUILD_INTERFACE:${CMAKE_CURRENT_LIST_DIR}/vanilla/include>)
