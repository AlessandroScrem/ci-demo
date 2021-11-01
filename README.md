[![Build Status](https://github.com/AlessandroScrem/ci-demo/actions/workflows/test.yml/badge.svg)](https://github.com/AlessandroScrem/ci-demo/actions/workflows/test.yml)
[![Coverage Status](https://coveralls.io/repos/github/AlessandroScrem/ci-demo/badge.svg?branch=main)](https://coveralls.io/github/AlessandroScrem/ci-demo?branch=main)
[![](http://github-actions.40ants.com/AlessandroScrem/ci-demo/matrix.svg)](https://github.com/AlessandroScrem/ci-demo/)


# gtest-demo

C/C++ unit test demo using [Google Test](https://code.google.com/p/googletest)
with continuous integration provided by [GitHub
Actions](https://docs.github.com/en/actions) 


## How to build this demo

```bash
git clone https://github.com/bast/gtest-demo.git
cd gtest-demo
cmake -S. -Bbuild 
cmake --build build
```


## Running the tests

Either using `ctest`:
```
$ cd build
$ ctest

Running tests...
Test project /home/user/gtest-demo/build
    Start 1: unit
1/1 Test #1: unit .............................   Passed    0.00 sec

100% tests passed, 0 tests failed out of 1

Total Test time (real) =   0.00 sec
```

Or directly using `unit_tests`:
```
$ cd build 
$ ./bin/unit_tests

[==========] Running 2 tests from 1 test case.
[----------] Global test environment set-up.
[----------] 2 tests from example
[ RUN      ] example.add
[       OK ] example.add (0 ms)
[ RUN      ] example.subtract
[       OK ] example.subtract (0 ms)
[----------] 2 tests from example (1 ms total)

[----------] Global test environment tear-down
[==========] 2 tests from 1 test case ran. (1 ms total)
[  PASSED  ] 2 tests.

```


## Acknowledgments

- Container Travis setup thanks to [Joan Massich](https://github.com/massich).
- Clean-up in CMake code thanks to [Claus Klein](https://github.com/ClausKlein).
- Clean-up and GitHub Actions workflow: [Roberto Di Remigio](https://github.com/robertodr).
