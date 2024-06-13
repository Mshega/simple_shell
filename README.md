# Simple Shell Project

Welcome to the Simple Shell project! This project involves creating a basic UNIX command line interpreter. The goal is to develop a functional shell that can execute commands, manage processes, and handle various built-in commands.

## Learning Objectives
By the end of this project, you should be able to explain:

- Who designed and implemented the original Unix operating system.
- Who wrote the first version of the UNIX shell.
- Who invented the B programming language (the direct predecessor to the C programming language).
- Who is Ken Thompson.
- How a shell works.
- What a PID and a PPID are.
- How to manipulate the environment of the current process.
- The difference between a function and a system call.
- How to create processes.
- The three prototypes of main.
- How the shell uses the PATH to find programs.
- How to execute another program with the execve system call.
- How to suspend the execution of a process until one of its children terminates.
- What EOF (end-of-file) is.
## Project Requirements
Create a UNIX command line interpreter with the following specifications:
## General
- Display a prompt and wait for user input.
- Execute simple command lines (no semicolons, pipes, or redirections).
- Each command line consists of one word with no arguments.
- If an executable is not found, print an error message and display the prompt again.
- Handle errors gracefully.
- Handle the "end of file" condition (Ctrl+D).
## Don't Implement
- PATH handling.
- Built-ins (initially).
- Special characters: ", ', `, , *, &, #.
- Cursor movement.
- Commands with arguments.
## Core Functionality
- Use execve for executing programs.
- Pass the environment to execve
## Features
## Simple Shell 0.1
- Handle command lines with arguments.
## Simple Shell 0.2
- Handle the PATH.
- Do not call fork if the command doesn’t exist.
## Simple Shell 0.3
- Implement the exit built-in to exit the shell (exit with no arguments).
## Simple Shell 0.4
- Implement the env built-in to print the current environment.
## Simple Shell 0.1+
- Write your own getline function.
- Use a buffer to read multiple characters at once.
- Use static variables.
- Do not use getline.
## Simple Shell 0.4+
- Handle arguments for the built-in exit (exit status).
## Simple Shell 1.0
- Implement setenv and unsetenv built-in commands.
- setenv VARIABLE VALUE: Initialize or modify an environment variable.
- unsetenv VARIABLE: Remove an environment variable.
- Implement the cd built-in command.
- cd [DIRECTORY]: Change the current directory.
- cd with no arguments should behave like cd $HOME.
- Handle cd -.
- Update the PWD environment variable.
- Implement the alias built-in command.
- alias [name[='value'] ...]: Define or display aliases.
## Simple Shell 1.0+
- Handle command files.
- simple_shell [filename]: Execute commands from a file without displaying a prompt.
## Usage
To use the Simple Shell, compile the code and run the executable. The shell will display a prompt and wait for commands. You can execute single-word commands, use built-in commands like exit and env, and utilize features like setenv, unsetenv, and cd.
## Commands
- exit: Exit the shell.
- env: Print the current environment.
- setenv VARIABLE VALUE: Set an environment variable.
- unsetenv VARIABLE: Unset an environment variable.
- cd [DIRECTORY]: Change the current directory.
- alias [name[='value'] ...]: Define or display aliases.
