# 🚀 Crafting an Interpreter in C

Hello everyone! 👋 I'm Sourav. I recently started learning C and diving into Data Structures and Algorithms (DSA). However, DSA felt a bit too theoretical on its own, so I decided the best way to really grasp these concepts is through project-based learning. 

What better way to see data structures in action than building a complete interpreter from scratch?

## 📖 The Journey

I am following Robert Nystrom's incredible guide, [Crafting Interpreters](https://www.craftinginterpreters.com/). 

Since I don't have a formal background in Java (which the first half of the book uses), I jumped straight into the deep end: **Part II: A Bytecode Virtual Machine in C**. Starting directly from **Section 14: Chunks of Bytecode**, this repository documents my daily progress, challenges, and code as I build the virtual machine.

## 🗓️ Progress Tracker

*   **Day 1:** Setting up the project, escaping the theory trap, and implementing the first bytecode chunks.
  *   **Day 2:** Implementing `chunk.c`, `chunk.h`, and `memory.h` for creating a Dynamic Array. 
*   **Day 3:** Added `debug.c`, `debug.h` & finally implemented the `main.c`. (Currently here! 📍)

## ✅ What's Implemented So Far

- **Bytecode Chunks:** A growable dynamic array (`Chunk`) to store compiled bytecode.
- **Memory Management:** Centralized `reallocate()` function with amortized-growth macros (`GROW_CAPACITY`, `GROW_ARRAY`).
- **Opcodes:** `OP_RETURN`.
- **Disassembler:** Basic instruction printer (`disassembleChunk`) for debugging bytecode contents.
- **Entry Point:** A working `main.c` that builds a chunk, writes an instruction, disassembles it, and cleans up memory.

> ## 🛠️ Tech Stack
*   **Language:** C
*   **Compiler:** GCC
*   **Architecture:** Bytecode Virtual Machine

## ⚙️ How to Build and Run

This project is compiled using standard GCC. To build and run the current codebase:

```bash
gcc main.c memory.c debug.c chunk.c -o main
./main