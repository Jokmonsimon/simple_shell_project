# Simple Shell Project

**A simple Unix command line interpreter**
![shell](/shell.png)

****
## Table of contents
 - **What is the shell?**
 - **About this project**
 - **Essential Functionalities of the Simple Shell**
 - **File description**
 - **List of allowed functions and system calls for this project**
 - **USAGE**
 - **Example of Usage**
 - **Bugs**
 - **TEAM**
 ****

## What is the shell?
The shell is a program that takes commands from the keyboard via the terminal, and gives them to the operating system to perform.\
**To better understand how the shell actually works, you can read our [Article].**

## About this project
This project is a simple version of the linux shell made for [ALX-SE Programme] taking part of the "Low-level programming & Algorithm - Linux and Unix system programming" projects.\
It is created using the **C programming Language** and it can do many functionalities that a real shell does.

## Essential Functionalities of the Simple Shell:
> Displays a prompt "#cisfun$ " and waits for user input.\
> Runs all commands of type "executable program" (ls and /bin/ls).\
> Runs the following build_in commands: **exit**, **env**, **setenv** and **unsetenv**.\
> Handles commands with arguments.\
> Handles the PATH global variable.\
> Handles The EOF (End Of File) condition.\
> Handles the Ctrl + C signal -> It doesn't exit the shell

## Files description
 - **AUTHORS** -> List of contributors to this repository
 - **man_1_simple_shell** -> Manual page for the simple_shell
 - **shell.h** -> Header file
 - **shell.c** -> main function
	- **sig_handler** -> handles the Ctrl + C signal
	- **_EOF** -> handles the End Of File condition
 - **string.c**
	- **_putchar** -> prints a character
	- **_puts** -> prints a string
	- **_strlen** -> gives the length of a string
	- **_strdup** -> copies a string in a newly allocated memory
	- **concat_all** -> concatenates 3 strings in a newly allocated memory
 - **line_exec.c**
	- **splitstring** -> splits a string into an array of words
	- **execute** -> executes a command using execve
	- **realloc** -> reallocates a memory block
	- **freearv** -> frees a 2 dimensional array
 - **linkpath.c**
	- **_getenv** -> returns the value of a global variable
	- **add_node_end** -> adds a node in a singly linked list
	- **linkpath** -> creates a singly linked list for PATH directories
	- **_which** -> finds the pathname of a command
	- **free_list** -> frees the linked list of PATH value
 - **checkbuild.c**
	- **checkbuild** -> checks if a command is a build-in command
 - **buildin.c**
	- **exitt** -> handles the exit buildin command
	- **_atoi** -> converts a string into an integer
	- **env** -> prints the current environment
	- **_setenv** -> Initialize a new global variable, or modify an existing one
	- **_unsetenv** -> remove a global variable

****
## List of allowed functions and system calls for this project
 - access (man 2 access)
 - chdir (man 2 chdir)
 - close (man 2 close)
 - closedir (man 3 closedir)
 - execve (man 2 execve)
 - exit (man 3 exit)
 - _exit (man 2 _exit)
 - fflush (man 3 fflush)
 - fork (man 2 fork)
 - free (man 3 free)
 - getcwd (man 3 getcwd)
 - getline (man 3 getline)
 - isatty (man 3 isatty)
 - kill (man 2 kill)
 - malloc (man 3 malloc)
 - open (man 2 open)
 - opendir (man 3 opendir)
 - perror (man 3 perror)
 - read (man 2 read)
 - readdir (man 3 readdir)
 - signal (man 2 signal)
 - stat (__xstat) (man 2 stat)
 - lstat (__lxstat) (man 2 lstat)
 - fstat (__fxstat) (man 2 fstat)
 - strtok (man 3 strtok)
 - wait (man 2 wait)
 - waitpid (man 2 waitpid)
 - wait3 (man 2 wait3)
 - wait4 (man 2 wait4)
 - write (man 2 write)
****

## USAGE
You can try our shell by following these steps:
> **Step 1:** Clone our repository using this command, (you need to have git installed on your machine first)
````
git clone https://github.com/Alphonse16/simple_shell.git
````
> **Step 2:** Change directory to simple_shell:
````
cd simple_shell
````
> **Step 3:** Compile the C files in this way:
````
gcc -Wall -Werror -Wextra -pedantic *.c -o hsh
````
> **Step 4:** Run the shell
````
./hsh
````
**Exiting the shell**
When you want to exit the shell, you can use one of the following methods:
> **1: Type the command "exit"**
````
exit
````
> **2: Press on Ctrl + D**

## Example of Usage
````
root@47a51ce69bf0:~/simple_shell# ls
AUTHORS  buildin.c  checkbuild.c  hsh  line_exec.c  linkpath.c  man_1_simple_shell  README.md  shell.c  shell.h  string.c
root@47a51ce69bf0:~/simple_shell# gcc -Wall -Werror -Wextra -pedantic -std=gnu89 *.c -o hsh
root@47a51ce69bf0:~/simple_shell# ./hsh
#cisfun$ /bin/ls
AUTHORS  buildin.c  checkbuild.c  hsh  line_exec.c  linkpath.c	man_1_simple_shell  README.md  shell.c	shell.h  string.c
#cisfun$ echo "/bin/ls" | ./hsh
"/bin/ls" | ./hsh
#cisfun$ echo Hello, This is an example
Hello, This is an example
#cisfun$ ls -l
total 68
-rw-r--r-- 1 root root   178 Aug 25 11:01 AUTHORS
-rw-r--r-- 1 root root  2187 Aug 25 09:15 buildin.c
-rw-r--r-- 1 root root   574 Aug 25 09:15 checkbuild.c
-rwxr-xr-x 1 root root 22456 Aug 25 11:07 hsh
-rw-r--r-- 1 root root  2111 Aug 25 09:15 line_exec.c
-rw-r--r-- 1 root root  2152 Aug 25 09:15 linkpath.c
-rwxr-xr-x 1 root root  1917 Aug 25 11:01 man_1_simple_shell
-rw-r--r-- 1 root root  5798 Aug 25 11:01 README.md
-rw-r--r-- 1 root root  1305 Aug 25 09:15 shell.c
-rw-r--r-- 1 root root  1385 Aug 25 09:15 shell.h
-rw-r--r-- 1 root root  1722 Aug 25 09:15 string.c
#cisfun$ exit
root@47a51ce69bf0:~/simple_shell#  
````
## Bugs
No known Bugs. Please email us if you find or experinece and bug(s).

## TEAM
* Ojok Simon Peter (simonpeter.oj@gmail.com)
* Mondliwethu Alphonse Hadebe (hmondliwethu@gmail.com)
