# Debugging with GDB

Learn to use GDB for debugging. If you need a quick reference, consider using a GDB cheat sheet.

## Launching GDB from a Text Editor

- In Emacs: Press `Escape` followed by `x`, then type `gdb`.
- Note: If you're using VS Code or another text editor, you might have different commands to launch GDB.

## GDB Commands

- **b (breakpoint)**: Sets a breakpoint where the program will pause its execution.
  - Example: `b eliminate.c:24`
  - Use `info b` to display information about all breakpoints.
- **bt**: Back trace — shows the call stack.
  - `f 0` is the current frame.
  - `f 1` is the calling frame.
- **r**: Run specific file.
- **c**: Continue execution until the next breakpoint.
- **n**: Advance to the next line of code.
- **display (variable)**: Monitor a variable's value without printing it.
  - Use `delete display` to stop monitoring.
- **print**: Evaluate and display the value of an expression.
- **info**: Display various information about the debugging state.
- **list**: Display source code.
- **f**: Select a specific frame in the call stack.

# C Files Syntax

```c
typedef struct
{
    // structure contents
} name;

name v1;  // create an instance of the type
```


# Homework Tips

- Use ASCII encoding.
- Count the number of occurrences of each letter.
- Reading a file in C:

  ```c
  FILE *fptr = fopen(filename,"r");
  if (fptr == NULL)
  {
      // Handle the error
  }
  int ch = fgetc(fptr);  // NOTE: Using unsigned char might cause issues with detecting EOF.







