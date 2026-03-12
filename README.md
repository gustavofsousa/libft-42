<h1 align="center">libft</h1>

<p align="center">
  <img src="https://img.shields.io/badge/language-C-blue.svg" alt="Language">
  <img src="https://img.shields.io/badge/42-School-black.svg" alt="42 School">
  <img src="https://img.shields.io/badge/status-complete-brightgreen.svg" alt="Status">
</p>

<p align="center">
  A complete reimplementation of the C standard library — from scratch, without using any of the original functions.
</p>

<p align="center">
  <a href="README.pt-br.md">🇧🇷 Leia em Português</a>
</p>

---

## Why this project matters

> "This project taught me how the C standard library actually works under the hood — how strings are traversed byte by byte, how memory is allocated and manipulated manually, and what it truly means to write reliable, reusable code."

Understanding these fundamentals is what separates a developer who *uses* tools from one who *understands* them. Every senior engineer working in systems programming, embedded, or performance-critical environments thinks at this level of abstraction.

---

## What was built

A fully functional personal C library (`libft.a`) covering:

### Memory
| Function | Description |
|---|---|
| `ft_memset` | Fill memory with a byte value |
| `ft_bzero` | Zero out a memory area |
| `ft_memcpy` | Copy memory areas |
| `ft_memmove` | Safe memory copy with overlap handling |
| `ft_memchr` | Locate byte in memory |
| `ft_memcmp` | Compare memory areas |
| `ft_calloc` | Allocate and zero-initialize memory |

### Strings
| Function | Description |
|---|---|
| `ft_strlen` | String length |
| `ft_strdup` | Duplicate a string |
| `ft_strchr` / `ft_strrchr` | Character search |
| `ft_strncmp` | String comparison |
| `ft_strlcpy` / `ft_strlcat` | Safe string copy and concat |
| `ft_strnstr` | Substring search |
| `ft_substr` | Extract substring |
| `ft_strjoin` | Join two strings |
| `ft_strtrim` | Trim characters from edges |
| `ft_split` | Split string by delimiter |
| `ft_strmapi` / `ft_striteri` | Functional map over string |

### Conversion
| Function | Description |
|---|---|
| `ft_atoi` | String to integer |
| `ft_itoa` | Integer to string |
| `ft_toupper` / `ft_tolower` | Character case conversion |

### Output
| Function | Description |
|---|---|
| `ft_putchar_fd` | Write char to file descriptor |
| `ft_putstr_fd` | Write string to file descriptor |
| `ft_putendl_fd` | Write string + newline |
| `ft_putnbr_fd` | Write integer |

### Linked Lists (Bonus)
| Function | Description |
|---|---|
| `ft_lstnew` | Create new node |
| `ft_lstadd_front` / `ft_lstadd_back` | Add node to front/back |
| `ft_lstsize` | Count list nodes |
| `ft_lstlast` | Get last node |
| `ft_lstdelone` / `ft_lstclear` | Delete node(s) |

---

## A standout technical detail

The implementation of `ft_split` correctly handles edge cases such as consecutive delimiters, leading/trailing delimiters, and empty strings — situations where many naive implementations silently fail or leak memory. This demonstrates careful thinking about boundary conditions, not just the happy path.

---

## Getting Started

```bash
git clone https://github.com/gustavofsousa/libft-42.git
cd libft-42
make
```

This produces `libft.a`. To use it in your project:

```c
#include "libft.h"
```

Compile with:
```bash
gcc your_file.c -L. -lft -o your_program
```

### Available make targets

| Target | Action |
|---|---|
| `make` | Build the library |
| `make bonus` | Build with linked list functions |
| `make clean` | Remove object files |
| `make fclean` | Remove object files and library |
| `make re` | Full rebuild |

---

## Skills demonstrated

- Manual memory management in C
- Pointer arithmetic and string manipulation
- Makefile and static library creation (`ar`)
- Defensive programming and edge case handling
- Linked list data structure implementation

---

## License

This project was developed as part of the [42 School](https://42.fr) curriculum.

---

<p align="center">Made with ☕ at 42 Rio de Janeiro</p>
