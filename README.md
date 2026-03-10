## 1. How to compile and run the shell

Step 1: Open a terminal

Step 2: Compile the program using the GCC

gcc myshell.c -o myshell

Step 3: Run the compiled shell program:

./myshell

You can entering commands now.

## 2. How to use the shell

The shell takes shortcut commands that map to standard Linux commands.

Available commands:

- C file1 file2  -----------Copy; create file2, copy all bytes of file1 to file2 without deleting file1.
- D file -----------------Delete the named file.
- E comment ---------- Echo; display comment on screen followed by a new line (multiple
spaces/tabs may be reduced to a single space)
- H ---------------------Help; display the user manual.
- L ----------------------List the contents of the current directory.
- M file -----------------Make; create the named text file by launching a text editor.
- P file -----------------Print; display the contents of the named file on screen.
- Q --------------------Quit the shell.
- W -------------------Wipe; clear the screen.
- X program -----------Execute the named program.

A command can be typed out like:

- linux(op20)|>E Hello World
- linux(op20)|>C file1.txt file2.txt
- linux(op20)|>L

## 3. Funciton used in the shell

parseCommand()
-Parses the user input into tokens and builds the argument array (argv) used for command execution.

printPrompt()
-Displays the shell prompt "linux(op20)|>" to the user.

readCommand()
-Reads a full line of input from the user using fgets().

commandExecution()
-Checks if the entered command is one of the shortcut commands and executes the corresponding Linux command using execvp().

## 4. Resources used

- lecture notes.
- https://www.geeksforgeeks.org/c/exec-family-of-functions-in-c/
- https://www.geeksforgeeks.org/c/making-linux-shell-c/
