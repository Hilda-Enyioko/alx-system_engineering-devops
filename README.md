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

