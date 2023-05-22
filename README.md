This is an alx proup poject by Alhassan Zainab and Michael Quartey.


0x16. C - Simple Shell

At the end of this project, we should be able to explain to anyone without the help of google;

1. Who designed and implemented the original Unix operating system
2. Who wrote the first version of the UNIX shell
3. 3Who invented the B programming language (the direct predecessor to the C programming language)
4. Who is Ken Thompson
5. How does a shell work
6. What is a pid and a ppid
7. How to manipulate the environment of the current process
8. What is the difference between a function and a system call
9. How to create processes
10. What are the three prototypes of main
11. How does the shell use the PATH to find the programs
12. How to execute another program with the execve system call
13. How to suspend the execution of a process until one of its children terminates
14. What is EOF / “end-of-file”?

list of allowed functions and system cals are;

access (man 2 access)
chdir (man 2 chdir)
close (man 2 close)
closedir (man 3 closedir)
execve (man 2 execve)
exit (man 3 exit)
_exit (man 2 _exit)
fflush (man 3 fflush)
fork (man 2 fork)
free (man 3 free)
getcwd (man 3 getcwd)
getline (man 3 getline)
getpid (man 2 getpid)
isatty (man 3 isatty)
kill (man 2 kill)
malloc (man 3 malloc)
open (man 2 open)
opendir (man 3 opendir)
perror (man 3 perror)
read (man 2 read)
readdir (man 3 readdir)
signal (man 2 signal)
stat (__xstat) (man 2 stat)
lstat (__lxstat) (man 2 lstat)
fstat (__fxstat) (man 2 fstat)
strtok (man 3 strtok)
wait (man 2 wait)
waitpid (man 2 waitpid)
wait3 (man 2 wait3)
wait4 (man 2 wait4)
write (man 2 write)

The shell should be compiled this way: gcc -Wall -Werror -Wextra -pedantic -std=gnu89 *.c -o hsh

the shell should work like this in interactive mode:
$ ./hsh
($) /bin/ls
hsh main.c shell.c
($)
($) exit
$


and like this in non-interactive mode:
$ echo "/bin/ls" | ./hsh
hsh main.c shell.c test_ls_2
$
$ cat test_ls_2
/bin/ls
/bin/ls
$
$ cat test_ls_2 | ./hsh
hsh main.c shell.c test_ls_2
hsh main.c shell.c test_ls_2
$

