# Project README

## Overview
This project is a simple C application that demonstrates the use of a parser library. The main functionality includes parsing and printing expressions, handling different data types, and pushing custom tokens into the parser.

## Features
- Parsing expressions (e.g., `int a = "hello world\n" + 10 + 0b1010101`)
- Classifying parsed tokens (e.g., converting strings to floats)
- Pushing custom tokens (e.g., string literals) into the parser
- Printing parsed results

## Project Structure
```
Cmd_Parser_Space/
├── build/              # .exe files produced by Main.c
├── src/                # source code
│   ├── Main.c          # Entry point
│   └── Parser.h        # Header file for the parser library
├── Makefile.linux      # Linux Build configuration
├── Makefile.windows    # Windows Build configuration
├── Makefile.wine       # Wine Build configuration
└── README.md           # This file
```

### Prerequisites
- C/C++ Compiler and Debugger (GCC, Clang)
- Make utility
- Standard development tools

## Build & Run
The project uses different Makefiles for building on Linux, Windows, and WebAssembly. The commands to build and run the application are as follows:

### Linux
```sh
cd Cmd_Parser_Space/
make -f Makefile.linux all
make -f Makefile.linux exe
```

### Windows
```sh
cd Cmd_Parser_Space/
make -f Makefile.windows all
make -f Makefile.windows exe
```

### WebAssembly (Emscripten)
```sh
cd Cmd_Parser_Space/
make -f Makefile.web all
make -f Makefile.web exe
```

### Notes
- The `build` directory will contain the executable files.
- The `src` directory contains only `Main.c` and its header file `Parser.h`.
- Each platform-specific makefile (`Makefile.linux`, `Makefile.windows`, `Makefile.wine`, `Makefile.web`) is designed to compile and run the application on that respective platform.