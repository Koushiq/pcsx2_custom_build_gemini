# PCSX2 Codebase Explanation

This document provides an overview of the PCSX2 codebase, including its file structure and general coding conventions.

## 1. File Structure Overview

The PCSX2 project has a well-organized structure to manage its various components. Here's a high-level overview of the main directories:

*   `3rdparty/`: Contains external libraries and their respective source code.
*   `bin/`: Holds compiled binaries, resources, and utility scripts.
*   `cmake/`: Contains CMake modules and scripts for building the project.
*   `common/`: Includes common utility functions, data structures, and shared components used across the project.
*   `pcsx2/`: The core PCSX2 emulator source code.
*   `pcsx2-gsrunner/`: Likely related to graphics testing or benchmarking.
*   `pcsx2-qt/`: Contains the source code for the Qt-based graphical user interface.
*   `tests/`: Unit tests and integration tests for various components.
*   `tools/`: Various development tools and scripts.
*   `updater/`: Contains the source code for the PCSX2 updater.

## 2. General Coding Conventions (C++)

While a formal style guide might exist elsewhere, here are some common C++ coding conventions observed in the PCSX2 codebase:

*   **Naming Conventions:**
    *   Classes: `PascalCase` (e.g., `MyClass`).
    *   Functions: `PascalCase` (e.g., `MyFunction`).
    *   Variables: `camelCase` (e.g., `myVariable`).
    *   Member Variables: Often prefixed with `m_` (e.g., `m_myMemberVariable`).
    *   Constants: `ALL_CAPS_WITH_UNDERSCORES` (e.g., `MY_CONSTANT`).
    *   Enums: `PascalCase` for the enum type, and `PascalCase` or `ALL_CAPS_WITH_UNDERSCORES` for enum values.

*   **Indentation:** Typically 4 spaces.

*   **Bracing Style:** Often uses K&R style for functions and Allman style for control structures.

*   **Comments:**
    *   Use `//` for single-line comments.
    *   Use `/* ... */` for multi-line comments.
    *   Doxygen-style comments are often used for API documentation.

*   **Include Guards:** Use `#pragma once` or traditional include guards (`#ifndef`, `#define`, `#endif`).

*   **Error Handling:** Exceptions are used in some parts, while others might rely on error codes or assertions.

*   **Smart Pointers:** `std::unique_ptr` and `std::shared_ptr` are commonly used for memory management.

*   **Modern C++ Features:** The codebase utilizes modern C++ features where appropriate, such as `auto`, range-based for loops, and `std::` algorithms.

*   **Platform-Specific Code:** Platform-specific code is typically encapsulated within preprocessor directives (e.g., `#ifdef _WIN32`).

This document will be updated as more specific conventions are identified or defined.
