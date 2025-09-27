# get_next_line 📝

[![Language](https://img.shields.io/badge/Language-C-blue)](https://github.com/khaledhajeid)
[![Platform](https://img.shields.io/badge/Platform-Linux%20%7C%20macOS-lightgrey)](https://github.com/khaledhajeid)
[![42 Project](https://img.shields.io/badge/42%20Project-Completed-brightgreen)](https://github.com/khaledhajeid)

---

## Overview
`get_next_line` is a **C function** that reads a file **line by line**, returning the next line with each call.  
This project was a key experience in understanding **file handling, dynamic memory allocation, and pointer management** in C.

---

## Features
- ✅ Reads **files line by line**, including very long lines.  
- ✅ Efficient **memory management** for each line.  
- ✅ Supports **multiple file descriptors** simultaneously.  
- ✅ Handles **edge cases**: empty files, files without a newline at the end.  

---

## Technologies
- Language: C
- Platform: Linux / macOS

---

## Usage

1. Include get_next_line.h in your project.
2. Compile your program along with get_next_line.c and get_next_line_utils.c.
3. Call get_next_line(int fd) to read the next line from the file descriptor fd.

```c
#include "get_next_line.h"
#include <fcntl.h>
#include <stdio.h>

int main(void)
{
    int fd = open("example.txt", O_RDONLY);
    char *line;

    while ((line = get_next_line(fd)) != NULL)
    {
        printf("%s", line);
        free(line);
    }
    close(fd);
    return 0;
}
```

---

## File Structure
```c
get_next_line/
├── get_next_line.c
├── get_next_line.h
├── get_next_line_utils.c
├── Makefile
└── README.md
```

---

## Project Highlights

- Strengthened low-level C programming skills.
- Practiced dynamic memory allocation and pointer manipulation.
- Built a robust and reusable function for efficient file reading.
- Successfully completed as part of the 42 school curriculum.
