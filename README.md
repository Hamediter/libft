*This project has been created as part of the 42 curriculum by [aboutale].*

# 📚 Libft - Your First C Library

<p align="center">
  <img src="https://img.shields.io/badge/Score-125%2F100-success?style=for-the-badge&logo=42" alt="Score">
  <img src="https://img.shields.io/badge/Language-C-blue?style=for-the-badge&logo=c" alt="C">
</p>

## 📝 Description
**Libft** is the foundational project of the 42 school curriculum. The goal is to recreate a set of functions from the standard C library (libc) as well as additional utility functions. 

Building this library from scratch provides a deep understanding of memory management, data structures, and the inner workings of C strings and linked lists. This library becomes a personal toolkit used in almost all subsequent 42 projects.

### Key Features
- **Libc Functions:** Re-implementation of standard functions (`strlen`, `memcpy`, `atoi`, etc.).
- **Additional Functions:** String manipulation (`ft_split`, `ft_strjoin`, `ft_itoa`).
- **Bonus Section:** Implementation of linked list management functions.

---

## 🏗️ Infrastructure Overview
The project is structured to be modular and easy to integrate:
- **Files:** Each function is contained in its own `.c` file for clarity and to optimize compilation.
- **Header:** `libft.h` contains all prototypes, macros, and the definition of the `t_list` structure.
- **Build System:** A robust `Makefile` that handles compilation, cleaning, and library archiving (`ar rcs`).

---

## 🛠️ Project Description & Design Choices

### Design Choices
*   **Memory Safety:** Every allocation (`malloc`) is strictly protected. In case of failure, my functions ensure no memory leaks occur before returning NULL.
*   **Performance:** Optimized loops and pointer arithmetic to mimic the efficiency of original libc functions.
*   **The "Norm":** The code strictly follows the 42 Norm (e.g., no more than 25 lines per function, restricted variable declarations), which forced me to find elegant, concise logic for complex problems like `ft_split`.
*   **Static Library:** The project compiles into a `.a` (static library) file, ensuring that only the used object files are included during the final linking process of external projects.

---

## 🚀 Instructions

### Prerequisites
- `gcc` or `clang` compiler.
- `make` (build automation tool).
- Standard C libraries.

### Step-by-Step Installation
1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/your-username/libft.git](https://github.com/your-username/libft.git) && cd libft
    ```
2.  **Compile the library:**
    
```bash
    make
    ```
    *Note: Use `make bonus` to include linked list functions.*

3.  **Clean build files:**
    ```bash
    make clean  # Removes objects
    make fclean # Removes objects and the .a library
    ```

4.  **Usage:**
    Include the header in your C code: `#include "libft.h"` and compile with `-L. -lft`.

---

## 📚 Resources

### References
- [C Standard Library Reference](https://en.cppreference.com/w/c/header) - Detailed documentation on standard C functions.
- [Makefile Tutorial](https://www.gnu.org/software/make/manual/make.html) - Understanding rules and variables.

### AI Usage
For this project, AI (Gemini/ChatGPT) was used for:
- **Refinement:** Explaining complex edge cases for functions like `memmove`.
- **Debugging:** Helping to understand memory alignment issues during testing.
- **Documentation:** Structuring this README to meet professional standards.
*No code was generated and used without a full manual review and adaptation to 42 Norm requirements.*
