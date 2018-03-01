# C++ Compiler Feature Support Checklist

This repository amalgamates information about public C++ compilers and their feature support.

Please feel free to correct and contribute via pull requests!

---

# Helpful Sources

* https://en.cppreference.com/w/cpp/compiler_support

---

# Legend
## Checkmarked Cell
Feature is fully supported, and no workarounds are needed.

## Blank Cell
Feature is either entirely unsupported, is missing and has the potential of being supported, or has simply been untested.

## Partial
Feature is only partially implemented and may require workarounds such as custom extensions.

---

# Checklist

## Backportable Features

| Compiler  | `nullptr` | `noexcept` | `override` | `final` | `static_assert` | `= delete` | `= default` | `char16_t` | `char32_t` |
|-----------|-----------|------------|------------|---------|-----------------|------------|-------------|------------|------------|
| MSVC2005  |           |            |            |         |                 |            |             |            |            |
| MSVC2008  |           |            |            |         |                 |            |             |            |            |
| MSVC2010  | ✓         |            |            |         | ✓               |            |             | ✓          | ✓          |
| MSVC2012  | ✓         |            | ✓          | ✓       | ✓               |            |             | ✓          | ✓          |
| MSVC2013  | ✓         |            | ✓          | ✓       | ✓               | ✓          | ✓           | ✓          | ✓          |
| MSVC2015  | ✓         | ✓          | ✓          | ✓       | ✓               | ✓          | ✓           | ✓          | ✓          |
| MSVC2017  | ✓         | ✓          | ✓          | ✓       | ✓               | ✓          | ✓           | ✓          | ✓          |
| Clang 2.9 | ✓         |            | ✓          | ✓       | ✓               | ✓          | ✓           | ✓          | ✓          |
| Clang 3.0 | ✓         | ✓          | ✓          | ✓       | ✓               | ✓          | ✓           |            |            |
| GCC 4.1.1 | ✓         |            | ✓          | ✓       | ✓               | ✓          | ✓           |            |            |
| GCC 4.3   | ✓         |            | ✓          | ✓       | ✓               | ✓          | ✓           |            |            |
| GCC 4.4   | ✓         |            | ✓          | ✓       | ✓               | ✓          | ✓           | ✓          | ✓          |
| GCC 4.6   | ✓         | ✓          | ✓          | ✓       | ✓               | ✓          | ✓           | ✓          | ✓          |
| GCC 4.7   | ✓         | ✓          | ✓          | ✓       | ✓               | ✓          | ✓           | ✓          | ✓          |
| GCC 4.9   | ✓         | ✓          | ✓          | ✓       | ✓               | ✓          | ✓           | ✓          | ✓          |

---

## Features that cannot be worked around

|  Compiler | `auto` decltype | Rvalue References | Variadic Templates | Range-Based `for` | Thread-Local Storage | Lambda Expressions | Strongly Typed Enumerations | Complex Data Member Initialisation | List & Aggregate Initialisation | `constexpr` | `std::move` | `std::unique_ptr` | `std::weak_ptr` | `std::shared_ptr` | `std::atomic` | `std::thread` | `std::mutex` | `std::lock_guard` | `std::async` | `std::function` | `std::chrono` |
|:---------:|:---------------:|:-----------------:|:------------------:|:-----------------:|:--------------------:|:------------------:|:---------------------------:|:----------------------------------:|:-------------------------------:|:-----------:|:-----------:|:-----------------:|:---------------:|:-----------------:|:-------------:|:-------------:|:------------:|:-----------------:|:------------:|:---------------:|:-------------:|
| MSVC2005  |                 |                   |                    |                   |                      |                    |                             |                                    |                                 |             |             |                   |                 |                   |               |               |              |                   |              |                 |               |
| MSVC2008  |                 |                   |                    |                   |                      |                    |                             |                                    |                                 |             |             |                   |                 |                   |               |               |              |                   |              |                 |               |
| MSVC2010  |                 |                   |                    |                   |                      |                    |                             |                                    |                                 |             |             |                   |                 |                   |               |               |              |                   |              |                 |               |
| MSVC2012  |                 |                   |                    |                   |                      |                    |                             |                                    |                                 |             |             |                   |                 |                   |               |               |              |                   |              |                 |               |
| MSVC2013  |        ✓        |         ✓         |          ✓         |         ✓         |                      |          ✓         |                             |                                    |                                 |             |             |                   |                 |                   |               |               |              |                   |              |                 |               |
| MSVC2015  |        ✓        |         ✓         |          ✓         |         ✓         |                      |          ✓         |                             |                                    |                                 |             |             |                   |                 |                   |               |               |              |                   |              |                 |               |
| MSVC2017  |        ✓        |         ✓         |          ✓         |         ✓         |                      |          ✓         |                             |                                    |                                 |             |             |                   |                 |                   |               |               |              |                   |              |                 |               |
| Clang 2.9 |                 |                   |                    |                   |                      |                    |                             |                                    |                                 |             |             |                   |                 |                   |               |               |              |                   |              |                 |               |
| Clang 3.0 |                 |                   |                    |                   |                      |                    |                             |                                    |                                 |             |             |                   |                 |                   |               |               |              |                   |              |                 |               |
| GCC 4.1.1 |                 |                   |                    |                   |                      |                    |                             |                                    |                                 |             |             |                   |                 |                   |               |               |              |                   |              |                 |               |
| GCC 4.3   |                 |                   |                    |                   |                      |                    |                             |                                    |                                 |             |             |                   |                 |                   |               |               |              |                   |              |                 |               |
| GCC 4.4   |                 |                   |                    |                   |                      |                    |                             |                                    |                                 |             |             |                   |                 |                   |               |               |              |                   |              |                 |               |
| GCC 4.6   |                 |                   |                    |                   |                      |                    |                             |                                    |                                 |             |             |                   |                 |                   |               |               |              |                   |              |                 |               |
| GCC 4.7   |                 |                   |                    |                   |                      |                    |                             |                                    |                                 |             |             |                   |                 |                   |               |               |              |                   |              |                 |               |
| GCC 4.9   |                 |                   |                    |                   |                      |                    |                             |                                    |                                 |             |             |                   |                 |                   |               |               |              |                   |              |                 |               |
