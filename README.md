# Libft

`libft` is a 42 project that recreates many useful C standard library functions and adds extra helper functions, including linked-list utilities.

The goal is to build a reusable static library that can be linked into future C projects.

## How to download

Clone the repository:

```bash
git clone https://github.com/mcarepa-42/libft.git
cd libft
```

Or download it from GitHub by clicking **Code** > **Download ZIP**, then extract the ZIP and open a terminal inside the project folder.

## Requirements

You need:

- `make`, if a Makefile is present;
- a C compiler such as `cc`, `gcc`, or `clang`.

## How to build

If the repository contains a Makefile, run:

```bash
make
```

This should create a static library, usually named:

```text
libft.a
```

If there is no Makefile in your downloaded version, you can manually compile the source files:

```bash
cc -Wall -Wextra -Werror -c *.c
ar rcs libft.a *.o
```

## How to use in another program

Create a small test file:

```c
#include "libft.h"
#include <stdio.h>

int main(void)
{
    printf("Length: %zu\n", ft_strlen("hello"));
    return 0;
}
```

Compile it with the library:

```bash
cc test.c libft.a -o test
./test
```

## Useful commands

```bash
make clean    # Remove object files
make fclean   # Remove object files and libft.a
make re       # Rebuild everything
```

## Included functionality

This library includes functions for:

- character checks and conversions;
- string manipulation;
- memory manipulation;
- number conversion;
- output to file descriptors;
- dynamic allocation helpers;
- linked-list operations.
