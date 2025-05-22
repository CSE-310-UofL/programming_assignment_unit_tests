include(FetchContent)

FetchContent_Declare(
  googletest
  URL https://github.com/google/googletest/archive/refs/tags/release-1.12.1.zip
  DOWNLOAD_EXTRACT_TIMESTAMP TRUE
)

FetchContent_MakeAvailable(googletest)

add_executable(RationalTests
    test_rational.cpp
    ../src/Rational.cpp
)

target_include_directories(RationalTests PRIVATE ../include)
target_link_libraries(RationalTests gtest gtest_main)

include(GoogleTest)
gtest_discover_tests(RationalTests)
