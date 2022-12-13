# Project 0x17.C - Simple Shell
       
#### Our goal of this project was to create a simple UNIX command interpreter or a simple shell that is capable of communicating with the operating system to execute commands given by the user.
       
## Basic working cycle of a shell

1. Shell initializes
2. A prompt is generated, waiting for user input
3. User input is tokenized and parsed
4. Command is executed if possible and result is returned
5. Shell generates prompt again returning to step 2
6. Shell terminates by typing `exit`

## Compilation & Execution

The program will be compiled with the following:

```
 gcc -Wall -Werror -Wextra -pedantic *.c -o hsh
```

To initiate the shell:

```
 ./hsh
```

Project completed by Josh Beeson & Jason Beagle
