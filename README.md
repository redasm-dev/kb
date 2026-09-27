# REDasm Knowledge Base (KB)
This repository contains the open-source, human-readable **TOML database** used by [REDasm Disassembler Engine](https://github.com/redasm-dev/core).  
It provides ready-to-use definitions for function signatures, library ordinals, `no_return` attributes, and compiler-specific heuristics and more.

## Database Structure & Coverage
*   **`arch/`**: Architecture-specific register layouts and metadata configuration files (`x86_32`, `x86_64`).
*   **`compiler/`**: Heuristics, type tables, and signatures for specific compiler toolchains (`msvc`, legacy `vb` / Visual Basic).
*   **`libc/`**: Universal C Standard Library definitions (`functions.toml`) used for auto-labeling known symbols during analysis.
*   **`os/`**: Operating system specific API definitions and subsystem layouts, covering modern, legacy, and embedded platforms (`android`, `linux`, `win16`, `win32`, `xbox`, `zxspectrum`).
*   **`pe/`**: Windows Portable Executable specific structure mappings and definitions (`types.toml`).
*   **`psx/`**: Native Sony PlayStation 1 BIOS function maps and signatures (`bios.toml`) for automated hardware preservation and homebrew reverse engineering.
