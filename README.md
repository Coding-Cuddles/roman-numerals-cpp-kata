# Roman numerals kata in C++

[![CI](https://github.com/Coding-Cuddles/roman-numerals-cpp-kata/actions/workflows/main.yml/badge.svg)](https://github.com/Coding-Cuddles/roman-numerals-cpp-kata/actions/workflows/main.yml)
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
 
This is a bootstrap repository for clean code katas in C++17 using GTest.

## Usage

You can import this project into [Replit](https://replit.com), and it will
handle all dependencies automatically.

### Prerequisites

* [CMake 3.19+](https://cmake.org)
* [Ninja](https://ninja-build.org)
* [GTest](https://github.com/google/googletest)

### Build

```console
make build
```

### Run main

```console
make run
```

### Run tests

```console
make test
```
