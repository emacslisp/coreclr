cmake_minimum_required(VERSION 2.8.12.2)

set(CMAKE_INCLUDE_CURRENT_DIR ON)

set(SOURCES
  _gcvt.c
)

add_executable(paltest_gcvt_test1
  ${SOURCES}
)

add_dependencies(paltest_gcvt_test1 CoreClrPal)

target_link_libraries(paltest_gcvt_test1
  pthread
  rt
  m
  CoreClrPal
)
