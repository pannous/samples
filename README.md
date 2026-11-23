# Warp Language Samples

This directory contains sample programs demonstrating various features of the Warp language, one folder per chapter
of the playground's guide (golf/ and wit/ aside).

## ✅ Working Samples (11)

These samples compile and run successfully:

- **simple.wap** - Basic arithmetic: `3*3`
- **fibonacci.wap** - Fibonacci sequence using recursion
- **factorial.wap** - Factorial calculation  
- **primes.wap** - Prime number checking
- **gcd.wap** - Greatest common divisor using Euclidean algorithm
- **sum.wap** - Sum of numbers 1-10
- **power.wap** - Exponentiation using recursion
- **collatz.wap** - Collatz conjecture sequence
- **ackermann.wap** - Ackermann function (recursive)
- **quadratic.wap** - Quadratic formula with √
- **fizzbuzz.wap** - Classic FizzBuzz problem

## 🔧 Feature Requirements

These samples need specific features to be implemented:

### String Operations
- **hello.wap** - String concatenation
- **comments.wap** - Comment parsing (parse-only demo)

### Module System
- **main.wap** - Uses `#use lib` directive
- **modules.wap** - Module import/export

### Advanced Math
- **sine.wap** - Needs τ and π constants, fraction literals
- **calculator.wap** - Complex expression parser

### Advanced Language Features
- **json_parser.wap** - Complex string manipulation
- **functions.wap** - Higher-order functions, lambdas
- **control_flow.wap** - Pattern matching, try/catch
- **async.wap** - Async/await support
- **binary_tree.wap** - Type definitions, optional types
- **quicksort.wap** - Array filter, lambda functions
- **mandelbrot.wap** - 2D arrays, complex iteration

### Data Structure Demos
- **data_structures.wap** - Syntax examples (no executable output)
- **types.wap** - Type system examples
- **html.wap** - HTML generation
- **html_dsl.wap** - DSL demonstrations

### Graphics & External Libraries  
- **raylib_*.wap** (3 files) - Raylib FFI examples
- **webgpu.wap** - WebGPU integration
- **visualizer.wap** - Winamp-style spectrum bars while a tune plays
- **gpu_visualizer.wap** - the same spectrum driving a raymarched WGSL tunnel with a pulsing gem (WebGPU)
- **gpu/lava_lamp.wap**, **gpu/northern_lights.wap**, **gpu/ringed_planet.wap** - WGSL fragment shaders of our own (`shader {…}` reading `$time`, `$mouse`, `$mouse_wheel`); the pointer turns the planet
- **gpu/rings.wap** - concentric rings coloured from two channel images generated in warp
- **gpu/kaleidoscope.wap** - a WGSL fragment shader: the pointer sets mirrors and zoom, a press lights the glass

Shaders by other authors (compute.toys and Shadertoy ports, which keep their authors' licenses) live in
https://github.com/pannous/shaders, folder warp/compute_toys: `warp <file>` runs them. warp itself ships only
shaders written for it.
- **sdl_red_square.wap** - SDL integration
- **test_ffi*.wap** (3 files) - FFI testing

### Complex Algorithms
- **game_of_life.wap** - Cellular automaton
- **neural_net.wap** - Neural network
- **sudoku.wap** - Sudoku solver
- **particles.wap** - Particle system

## Running Samples

```bash
# Run a working sample
cargo run -- samples/functions/fibonacci.wap

# Or use the test suite
cargo test --test test_samples
```

## Adding New Samples

When adding a new sample:
1. Add it to the folder of its guide chapter, `samples/<chapter>/` (graphics, sound, text …: the playground menu's
   groups, notes/samples.md), with `.wap` extension, and name it in that chapter's `Examples:` line of web/playground/guide.md
2. If it should work, add a test in `tests/programs/test_samples.rs`
3. Use `#[ignore]` attribute with explanation if feature not yet implemented
4. Update this README

## Current Test Status

```bash
cargo test --test test_samples
# 11 passed; 0 failed; 3 ignored
```
