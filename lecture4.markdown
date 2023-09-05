Learn gdb to debug (go to hotseat)

emacs is a text editor (vs code is fine)

use file eliminate to test if it's an executable file

To go to gdb from text editor, press escape and x, then type gdb

P.S. you could use a gdb cheat sheet

GDB COMMAND

b - a break point, the program would stop at the break point, it would stop at that line but not executing it
    b eliminate.c:24
    info b - show the information of all the break points

bt - back trace? what does it do? f 0 is current frame, and f 1 is who calls it
     show the stack memory, solve recursion question

r - run specific file

c - continue, go to next breakpoint

n - you go to next line

display (variable) - it works like a print but not actual print it
delete display - delete the display function

print - similar to the print command in C

info - get info

lsit - show ten lines something?

f - go to specific frame


Files
    
Syntax:

tydef struct
{

}(name)

(name) v1; // create an example of that type

create new data type is to
    - organize the information better
    - distinguish data types from an object
    - improve consistency

sizeof(type) - this would tell you the size of that data type



Homework tips
- use ASCII
- need to count the number of letters appeared
- open the file
    FILE * fptr = fopen(filename,"r")
    if (fptr == NULL)
    {
        //do not fclose in here
    }
    int ch = fgetc(fptr); //if you do unsigned char, you could never reach/detect the end of the file since EOF is -1

grep - is to search this symbol in a file and output any line that includes the symbol

file is like a river, the marker is upstream, as you read you go downstream.

ftell - is a function that tells you where in the file.
fseek - go to the specific location



