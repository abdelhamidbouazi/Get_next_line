# get_next_line

`get_next_line` is a function that reads a line from a file descriptor and returns it as a string. This project is part of the curriculum at 42, and is designed to help students learn about file input/output and memory allocation.

## Usage

To use the `get_next_line` function, simply include the header file in your program and call the function with a file descriptor as the first parameter. The function will return a pointer to a string containing the next line in the file.

```c
#include "get_next_line.h"

int main()
{
    int fd;
    char *line;

    fd = open("file.txt", O_RDONLY);
    while ((line = get_next_line(fd)) != NULL)
    {
        // do something with the line
        free(line);
    }
    close(fd);
    return (0);
}
