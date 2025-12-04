# Shell Variables & Expansions — Project Overview

This project introduces core concepts of the Linux shell environment, with a strong focus on variables, expansions, initialization files, arithmetic, aliases, and command execution.  
Each task is implemented as a small Bash script that demonstrates a specific concept.

---

## 📌 Core Concepts

### 1. **Shell Initialization Files**
These are scripts that run automatically when a shell session starts.

- **`/etc/profile`**  
  Runs for all users when they log in. Sets system-wide environment variables.

- **`/etc/profile.d/`**  
  Contains multiple shell scripts that extend `/etc/profile` functionality.

- **`~/.bashrc`**  
  Runs for non-login interactive shells.  
  Users commonly place aliases, functions, PATH additions, and custom settings here.

---

### 2. **Variables in the Shell**

- **Local variables**  
  Only available in the current shell.

- **Global variables (Environment variables)**  
  Exported using `export`, and inherited by child processes.

- **Reserved variables**  
  Special variables the shell uses internally.  
  Examples:
  - `HOME` → user home directory  
  - `PATH` → directories to search for commands  
  - `PS1` → the shell prompt format  

- **Special parameters**
  - `$?` → exit status of the last command  
  - `$0`, `$1`… → script name and arguments  
  - `$$` → process ID of current shell  

---

### 3. **Expansions**

- **Variable Expansion** — `$VAR`  
- **Command Substitution** — `$(command)` or backticks  
- **Arithmetic Expansion** — `$(( expression ))`  
- **Filename Expansion (Globbing)** — `*.txt`, `?.sh`, etc.  

**Single quotes `' '`** preserve literal text.  
**Double quotes `" "`** allow expansion inside them.

---

### 4. **Aliases**

Aliases help shorten commands:

```bash
alias ll='ls -l'
```
Disable temporarily:

\ls

List aliases:

alias


---

5. Executing Commands from a File

The dot operator executes commands in the current shell:

. script.sh

Same as:

source script.sh

This allows variables to persist in the current environment.


---

## Task Breakdown

Below is a summary of each script and the concept it demonstrates.


---

0. 0-alias

Creates an alias named ls that runs rm *.
Demonstrates the alias command.


---

1. 1-hello_you

Prints:
hello <current_user>
Uses variable expansion and $USER.


---

2. 2-path

Adds /action to the end of the PATH.
Shows how to modify global PATH.


---

3. 3-paths

Counts how many directories are in $PATH.
Uses string manipulation and command substitution.


---

4. 4-global_variables

Prints the environment variables using printenv.
Demonstrates global vs local variables.


---

5. 5-local_variables

Lists all local and global variables plus shell functions.
Uses the set command.


---

6. 6-create_local_variable

Creates a local variable BEST="School".
Shows how to define variables in Bash.


---

7. 7-create_global_variable

Creates a global variable using export.
Shows the difference between local and environment variables.


---

8. 8-true_knowledge

Prints:
128 + $TRUEKNOWLEDGE
Demonstrates arithmetic expansion.


---

9. 9-divide_and_rule

Calculates POWER / DIVIDE.
Uses arithmetic expansion on environment variables.


---

10. 10-love_exponent_breath

Computes BREATH ^ LOVE.
Shows the use of ** exponent operator.


---

11. 11-binary_to_decimal

Converts binary to decimal using arithmetic expansion:
$((2#binary_number)).


---

12. 12-combinations

Prints all two-letter combinations from aa to zz, except oo.
Demonstrates:

loops

ASCII ranges

condition checks



---

13. 13-print_float

Prints a number with two decimal places using printf.


---

14. 100-decimal_to_hexadecimal

Converts a decimal number to hexadecimal using:
printf "%x\n" "$DECIMAL".


---

15. 101-rot13

Encodes/decodes text using ROT13.
Uses the tr command.


---

16. 102-odd

Prints every other line of input.
Uses sed -n 'p;n' or shell logic.


---

17. 103-water_and_stir

Adds two numbers from custom bases:

WATER → base water

STIR → base stir

Result in base bestchol


Demonstrates:

custom base conversion

creative manipulation using tr + arithmetic



---

## Requirements Summary

All scripts must be 2 lines only (except the shebang)

Must be executable

Must follow Bash syntax

No: &&, ||, ;, sed, awk, bc

First line:

#!/bin/bash
