# Lecture 5

## Quick Sort

- There would be a pivot
- Partition the array into two parts
- It's an example of recursive algorithm

**Why is bubble sort bad?**
it does not ultilize the transitivity of the comparison

typically, we would choose the first element as the pivot




## Number System
1. Decimal: base 10 -> 0 1 2 3 4 5 6 7 8 9 (**512.34 = 5 * 10^2 + 1 * 10^1 + 2 * 10^0 + 3 * 10^-1 + 4 * 10^-2**)
2. Binary: base 2 -> 0 1 
3. Octal: base 8 -> 0 1 2 3 4 5 6 7
4. Hexadecimal: base 16 -> 0 1 2 3 4 5 6 7 8 9 A B C D E F (**B9C6 = 11 * 16^3 + 9 * 16^2 + 12 * 16^1 + 6 * 16^0 = 47558, 7B9.C6 = 7 * 16^2 + 11 * 16^1 + 9 * 16^0 + 12 * 16^-1 + 6 * 16^-2 = 197.7734375**)

```c
printf("%d, %c", 65, 65);
```

## ASCII (some hints about hw3)

```c
char sum[128] = {0};

while{!feof(fptr)}
{
    int ch = fgetc(fptr);
    if((ch >= 'A' && ch <= 'Z') || (ch >= 'a' && ch <= 'z'))
    {
        sum[ch]++;
    }
}

```

# reading numbers from a file

**if you do fgetc, the number -598 would be store as 5, 9, 8**

**We should use fscanf instead**

```c
//different ways to read a file
int fgetc(FILE * stream);

char * fgets(char *str, int size, FILE *stream);
//1st arg is the space you want to store the string
//2nd arg is the size of the string, this should be the size of the 1st arg
//3rd arg is the file you want to read from
//don't use gets
//if a newline is read, it is stored into the buffer

int fscanf(FILE *stream, const char *format, ...);
int x;
int y;
fscanf(fptr, "%d %d", &x, &y);
```

```c
#include <stdio.h>
#include <stdlib.h>

int fseek(FILE *stream, long offset, int whence);


int ftell(FILE *stream);
//return the current position of the file pointer
//example
``````

**different functions read different sizes**


```c
fprintf(FILE *stream, const char *format, ...);
```

## Homework 5
1. C does not has "string" data type
2. C uses "array of characters + \0" to represent a string
3. Each element can store a value between 0 and 255
4. Conversion between numbers and characters based on ASCII table

```c
size_t strlen(); //it excludes the null character
char * strcpy(char *dest, const char *src);
//the const is to make sure you don't change the source

char * arr1;
arr1 = malloc(sizeof(char) * 10);

strcpy(arr1, "hello");

char arr2[10];

free(arr1);

//&arr[k] = &arr[0] + k * sizeof(arr[0])

```

**in C, the double quote add a null character at the end of the string**
**an array is always a pointer**
**but a pointer is not always an array**


**gotta make sure source and destination are not overlapping**
```c
//case when source and destination are overlapping
char arr[10] = "hello";
strcpy(arr + 1, arr);
```





