# Chip-8 Emulator

This is my personal **Chip-8 emulator** project written in C++.  
I am currently learning C++ and decided to build this emulator from scratch.  
The project uses **C++17 (GCC 15.2.0)** and **SDL3** for graphics and input.

---

## Table of Contents


- [Installation](#installation)
- [Folder Structure](#folder-structure)
- [Building the Emulator](#building-the-emulator)
- [Running a ROM](#running-a-rom)
- [Debug Mode](#debug-mode)
- [Cleaning the Build](#cleaning-the-build)
- [Documentation & References](#documentation--references)

---

## Installation

> **Note:** These instructions are for **macOS**. Linux users can install `g++`, `make`, and `SDL3` using their package manager. Windows support is not fully tested and may be buggy.

### Step 1: Install Homebrew (if not already installed)

```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```


### Step 2: Install SDL3

```bash
brew install sdl3

```


### Step 3: Install g++ and make (if havent)
```bash
brew install gcc make
```



### Step 4: Clone this repo
```bash
git clone https://github.com/nhantran1711/chip8emulator.git
cd chip8emulator

```
---

## Folder Structure

```bash
chip8emulator/
├─ chip8.cpp          # Main emulator source code
├─ Makefile           # Makefile for building and debugging
├─ roms/              # Place your Chip-8 ROM files here
│   └─ invaders.rom 
├─ test/              # Optional test ROMs or scripts
├─ README.md          # This file
├─ chip8              # Compiled executable (after make)
└─ chip8.dSYM         # Debug symbols (MacOS, after debug build)
```

Place all ROM files you want to run in the roms/ folder.

test/ can hold any ROMs or testing scripts you want to try.


## Building emulator

Make sure you are in the project root folder (chip8emulator) before running:



# Standard Build


```bash
make
```

This will generate executable ./chip8 file 



# Development Build


---
## Debug 


```bash
make debug
```

This will generate ./chip8 file and debug screen


## Running a rom

```bash
./chip8 roms/<romfile.rom>
```



# Example
```bash
./chip8 roms/invaders.rom 

# or

./chip8 "roms/invaders.rom"

```


**Important**: Always run from the project root so relative paths like roms/ work correctly.


## Debug Mode


```bash
make debug
./chip8 roms/"IBM Logo.ch8"
# or using escaped space
./chip8 roms/IBM\ Logo.ch8
```



## Cleaning after build

Remove executable and debug symbols


```bash
make clean
```



## Documentation & References

A huge thanks to the following resources that helped me a lot:

- **SDL Wiki (SDL3 Documentation)**  
  [https://wiki.libsdl.org/SDL3/FrontPage](https://wiki.libsdl.org/SDL3/FrontPage)

- **How to Write an Emulator (Chip-8 Interpreter)**  
  [https://multigesture.net/articles/how-to-write-an-emulator-chip-8-interpreter/](https://multigesture.net/articles/how-to-write-an-emulator-chip-8-interpreter/)

- **Codeslinger – Chip-8 Projects**  
  [http://www.codeslinger.co.uk/pages/projects/chip8.html](http://www.codeslinger.co.uk/pages/projects/chip8.html)
