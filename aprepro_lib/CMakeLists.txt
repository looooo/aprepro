SET(APREPRO_VERSION_MAJOR "4")
SET(APREPRO_VERSION_MINOR "02")
SET(APREPRO_VERSION_PATCH "0")
SET(APREPRO_VERSION "${APREPRO_VERSION_MAJOR}.${APREPRO_VERSION_MINOR}")
SET(APREPRO_VERSION_FULL "${APREPRO_VERSION}.${APREPRO_VERSION_PATCH}")

INCLUDE_DIRECTORIES(
  ${CMAKE_CURRENT_SOURCE_DIR}
)

SET(APREPRO_HEADERS
  aprepro.h
)


SET(SOURCES
 apr_aprepro.cc 
 apr_util.cc 
 apr_stats.cc 
 apr_init.cc 
 apr_builtin.cc 
 apr_units.cc 
 apr_tokenize.cc
 apr_scanner.cc  
 apr_getline_int.c
 apr_array.cc
 apr_parser.cc
)

add_library(aprepro_lib SHARED ${APREPRO_HEADERS} ${SOURCES})
install(TARGETS aprepro_lib DESTINATION ${CMAKE_INSTALL_PREFIX}/lib)