INCLUDE_DIRECTORIES(
  ${CMAKE_CURRENT_SOURCE_DIR}
  ${CMAKE_CURRENT_BINARY_DIR}
  "../aprepro_lib"
)


ADD_EXECUTABLE(aprepro aprepro.C)
target_link_libraries(aprepro aprepro_lib)
install(TARGETS aprepro DESTINATION ${CMAKE_INSTALL_PREFIX}/bin)
