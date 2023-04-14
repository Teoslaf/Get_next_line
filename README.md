Project Description

The aim of this project is to write a function that can read a line from a file descriptor, one line at a time. The function should be able to handle different file descriptors and return NULL if there is nothing else to read or an error occurred.
Functionality

The function is named get_next_line and has the following prototype:

arduino

char *get_next_line(int fd);

The function takes a file descriptor fd as a parameter and returns a string containing the line read from the file descriptor. The function should be called repeatedly in a loop to read the text file pointed to by the file descriptor, one line at a time.

The returned line should include the terminating \n character, except if the end of file was reached and does not end with a \n character.

If there is nothing else to read or if an error occurred, the function should return NULL.
Usage

To compile the program, you should add the option -D BUFFER_SIZE=n to define the buffer size for read(). You can choose the default value of your choice.

The program should be compiled using the following command:

mathematica

cc -Wall -Wextra -Werror -D BUFFER_SIZE=42 <files>.c

The program should also be able to compile without the -D BUFFER_SIZE flag.
Bonus Part

If you have completed the mandatory part of the project, you can attempt the bonus part. In the bonus part, you should develop the get_next_line function using only one static variable. The function should be able to manage multiple file descriptors at the same time.
Files

The project consists of the following files:

    get_next_line.c
    get_next_line_utils.c
    get_next_line.h

If you attempt the bonus part, you should also include the following files:

    get_next_line_bonus.c
    get_next_line_utils_bonus.c
    get_next_line_bonus.h

Forbidden Functions

    You are not allowed to use your own libft library.
    You are not allowed to use the lseek() function.
    Global variables are forbidden.

External Functions

    read()
    malloc()
    free()
