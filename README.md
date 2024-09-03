# `echo` command from scratch in C

This is a simple implementation of `echo` command in _Unix-like systems_ from scratch, in _C_.

> The program prints the arguments passed to it, with an option to suppress the newline at the end.

## How It Works

- There are two header files: `stdio.h` for input/output functions and `string.h` for string manipulation functions.

- The main function takes in two parameters:
  - `argc`: The number of command-line arguments.
  - `argv`: An array of strings representing the command-line arguments.

- The program iterates over the arguments starting from _index 1_ (since _index 0_ is the program's name).

- If the `-n` flag is found, the program sets the `newline` variable to _0_, indicating that no _newline_ should be printed after the output.

- For each argument that is not `-n`, the program prints it followed by a space (except after the last argument).

- Finally, if the `newline` variable is still set to _1_, the program prints a _newline_ character.

## Compilation

To compile the program, run the following command in your terminal:

```bash
gcc -o echo main.c
```

This command will generate an executable named `echo`.

## Usage

Compiled program can be invoked as follows:

```bash
./echo [options] [arguments]
```

### Examples

- Basic Usage:

```bash
./echo Hello, World!

> Hello, World!
```

- Suppressing Newline:

```bash
./echo -n Hello, World!

> Hello, World! (No newline at the end)
```

- Multiple Arguments:

```bash
./echo Hello this is a test.

> Hello this is a test.
```

- Using Environment Variables:

```bash
export $VAR="this is a test"
./echo Hello $VAR World $RANDOM

> Hello this is a test World 27453
```
