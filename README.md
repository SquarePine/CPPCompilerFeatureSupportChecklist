# C++ Compiler Feature Support Checklist

This repository amalgamates information about public C++ compilers and their feature support.

# Legend
## Checkmarked Cell
Feature is fully supported, and no workarounds are needed.

## Blank Cell
Feature is either entirely unsupported, or is missing and has the potential of being supported.

## Partial
Feature is only partially implemented and may require workarounds such as custom extensions.

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

## Features that cannot be worked around
