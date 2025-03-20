cmake_minimum_required(VERSION 3.5)

project(
  gsl
  VERSION 3.1.0
  DESCRIPTION "Guidelines Support Library"
  HOMEPAGE_URL "https://github.com/microsoft/GSL"
  LANGUAGES CXX)

include(GNUInstallDirs)

add_library(gsl INTERFACE)

target_include_directories(
  gsl INTERFACE $<BUILD_INTERFACE:${CMAKE_CURRENT_LIST_DIR}/vanilla/include>
                $<INSTALL_INTERFACE:${CMAKE_INSTALL_INCLUDEDIR}>)

# install(TARGETS gsl EXPORT Microsoft.GSLConfig) install(DIRECTORY
# vanilla/include/gsl DESTINATION ${CMAKE_INSTALL_INCLUDEDIR})

# install( EXPORT Microsoft.GSLConfig NAMESPACE Microsoft.GSL:: DESTINATION
# ${CMAKE_INSTALL_DATADIR}/cmake/Microsoft.GSL) export( TARGETS gsl NAMESPACE
# Microsoft.GSL:: FILE Microsoft.GSLConfig.cmake)
