# Roman numerals kata in C++

[![CI](https://github.com/Coding-Cuddles/roman-numerals-cpp-kata/actions/workflows/main.yml/badge.svg)](https://github.com/Coding-Cuddles/roman-numerals-cpp-kata/actions/workflows/main.yml)
[![C++17](https://img.shields.io/badge/C%2B%2B-17-blue.svg)](https://en.cppreference.com/w/cpp/17)
[![License: MIT](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)
[![Replit](https://img.shields.io/badge/Try%20with%20Replit-black?logo=replit)](https://replit.com/new/github/Coding-Cuddles/roman-numerals-cpp-kata)

## Overview

This kata complements [Clean Code: Advanced TDD, Ep. 19](https://cleancoders.com/episode/clean-code-episode-19-p1).

This repository contains two exercises designed to improve your skills in
test-driven development.

## Instructions

Roman numerals are a numeral system that was used by ancient Rome. Numbers in
this system use letters from the Latin alphabet. Currently, it uses seven
symbols:

| Symbol | Value |
|:-------|-------|
| I      | 1     |
| V      | 5     |
| X      | 10    |
| L      | 50    |
| C      | 100   |
| D      | 500   |
| M      | 1000  |

Instead of writing the same letter four times, a rule for subtraction is used:
the letter is written once, then the next largest Roman numeral is written.
For example, 4 is not written as IIII, but instead as IV, because IV is V (5)
minus I (1).

In general, the values for 5, 50, and 500 are not subtracted.

### Exercise 1

The task at hand entails crafting a function `to_roman(number: int) -> str` to
convert regular Arabic numbers into Roman numerals, such as:

* 4 → IV
* 7 → VII
* 9 → IX

The lowest number you can write in Roman Numerals is number I (1). And the
largest numeral is MMMCMXCIX (3999).

### Exercise 2

In this phase, the objective is to develop a function `from_roman(number: str)
-> int` that performs the reverse conversion, transforming Roman numerals into
their corresponding Arabic digits.

## Guiding Principles

* If you don't know an existing algorithm, follow the principles of strict
  Test-Driven Development (TDD) to derive one.
* Reflect on whether the sequence in which you write tests influences the final
  design of your algorithm.
* Consider whether it's more beneficial to devise an algorithm before embarking
  on TDD, especially if you don't already know one.
* If you do know an algorithm, evaluate if it can be implemented using strict
  TDD principles.
 
This is a C++17 kata using GoogleTest. Setup is complete when CTest reports
`100% tests passed`.

## Prerequisites

Required:

- [Git](https://git-scm.com/downloads)
- A compiler with C++17 support. Choose one:
  - [GCC](https://gcc.gnu.org/) 10+ on Linux
  - [LLVM Clang](https://llvm.org/) 14+ on Linux
  - [Apple Clang](https://developer.apple.com/xcode/) 17+ on macOS
  - [MSVC](https://visualstudio.microsoft.com/) 2022 on Windows
- [CMake 3.24 or later](https://cmake.org)

Optional:

- [GNU Make](https://www.gnu.org/software/make/), for shorter commands. Every
  required task also has direct CMake and CTest commands. Make may be
  unavailable on Windows.

You do not need to install GoogleTest separately. CMake finds an installed
copy or downloads the pinned release when needed.

## Set up the kata

You can also import the project into [Replit](https://replit.com), which
provides the required dependencies.

1. Clone the repository:

   ```console
   git clone https://github.com/Coding-Cuddles/roman-numerals-cpp-kata.git
   ```

2. Enter the repository directory:

   ```console
   cd roman-numerals-cpp-kata
   ```

3. Build and run the tests. Use Make when it is installed:

   ```console
   make test
   ```

   Otherwise, use CMake and CTest directly:

   ```console
   cmake -S . -B build -DCMAKE_BUILD_TYPE=Debug
   cmake --build build --config Debug
   ctest --test-dir build --build-config Debug --output-on-failure
   ```

The first run may download and build GoogleTest. CTest should report
`100% tests passed`. If a command reports a missing compiler or CMake, install
that prerequisite and run the setup commands again. Setup is complete when
CTest reports `100% tests passed`.

## Work on the kata

Add one test at a time to `test_roman_numerals.cpp`, then implement enough code
in `roman_numerals.h` to make the test pass. Keep the existing exercises and
constraints above as the target behavior.

After each change, use Make when it is installed:

```console
make test
```

Otherwise, use CMake and CTest directly:

```console
cmake --build build --config Debug
ctest --test-dir build --build-config Debug --output-on-failure
```

Continue when CTest reports `100% tests passed`.

## Run the example

Use Make when it is installed:

```console
make run
```

Otherwise, use the CMake run target:

```console
cmake --build build --config Debug --target run
```

The executable prints `Hello World!`.

## Make command reference

Make is optional. Run `make` or `make help` to list these commands in the
terminal.

| Command             | Result                                    |
| ------------------- | ----------------------------------------- |
| `make all`          | Build and run the test suite              |
| `make help`         | List public Make targets                  |
| `make build`        | Configure and build without running tests |
| `make run`          | Build and run the example executable      |
| `make test`         | Build and run the test suite              |
| `make format`       | Format tracked C++ and header files       |
| `make format-check` | Check formatting without changing files   |
| `make clean`        | Remove generated build artifacts          |
